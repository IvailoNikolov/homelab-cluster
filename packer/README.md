# instal-packer
1. sudo mkdir -m 0755 -p /etc/apt/keyrings/
2. curl -fsSL https://apt.releases.hashicorp.com/gpg |
    sudo gpg --dearmor -o /etc/apt/keyrings/gpg
3. echo "deb [signed-by=/etc/apt/keyrings/gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gp
g.list > /dev/null
4. sudo apt-get update && sudo apt-get install packer
6. packer --version
7. # Optional (you can find the email address / ID using `apt-key list`)
sudo apt-key del support@example.com
8. # Optional (not necessary on most systems)
sudo chmod 644 /etc/apt/keyrings/gpg
sudo chmod 644 /etc/apt/sources.list.d/gpg.list