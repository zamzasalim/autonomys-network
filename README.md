<p style="font-size:14px" align="right">
<a href="https://t.me/airdropasc" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" width="30"/></a>
</p>

<p align="center">
  <img height="300" height="auto" src="https://raw.githubusercontent.com/zamzasalim/logo/main/1.png">
</p>


# Autonomys Network Node & Farmer

## Siapkan Wallet Subwallet & Get Address
- Download Extensi [Subwallet](https://chromewebstore.google.com/detail/subwallet-polkadot-wallet/onhogfjeacnfoofkfgppdlbmlmnplgbn)
- Create wallet & backup
- Open web : [Autonomys](https://astral.autonomys.xyz/gemini-3h/consensus?walletSidekick=open)
- Konek Subwallet
- Copy Address & Paste address waktu penginstalan node
## Auto Install
```
wget https://raw.githubusercontent.com/zamzasalim/autonomys-network/main/autonomys.sh && chmod +x autonomys.sh && ./autonomys.sh
```
- Paste Address Autonomys
- Set port (kalo gk mau langsung enter aja)
- Set SSD (isi 200G)
- Lalu enter enter sampe selesai install
## Start Node
```
sudo systemctl start subspace-node && sudo systemctl start subspace-farmer
```
## Enable Node
```
sudo systemctl enable subspace-node && sudo systemctl enable subspace-farmer
```
# Perintah Berguna
## Check Status Node
```
sudo systemctl status subspace-node
```
## Check Status Farmer
```
sudo systemctl status subspace-farmer
```
## Check Log Node
```
sudo journalctl -f -o cat -u subspace-node
```
## Check Log Farmer
```
sudo journalctl -f -o cat -u subspace-farmer
```
## Stop Node
```
sudo systemctl stop subspace-node && sudo systemctl stop subspace-farmer
```
## Disable Node
```
sudo systemctl disable subspace-node && sudo systemctl disable subspace-farmer
```
## Delete Node (Kalo dah end nodenya)
```
sudo systemctl stop subspace-node && sudo systemctl stop subspace-farmer && \
sudo systemctl disable subspace-node && sudo systemctl disable subspace-farmer && \
sudo rm /etc/systemd/system/subspace-node.service /etc/systemd/system/subspace-farmer.service && \
sudo userdel -r subspace && \
sudo rm -rf /home/subspace/.local/bin/subspace-node /home/subspace/.local/bin/subspace-farmer /home/subspace/.local/share/subspace-node /home/subspace/.local/share/subspace-farmer && \
sudo systemctl daemon-reload
```
