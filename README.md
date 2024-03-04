# Fairblock Testnet (Validator Setup)
<img src="https://github.com/hakandemirdev/Fairblock_Testnet/blob/e4971c7085f4b66a19c36fb50bffb54ecebdb81e/fairblocklogo.png" width="auto">

Öncelikle işletim sistemimizi güncelliyoruz.Ubuntu 22.04.3 LTS üzerine kurdum.
```
sudo apt update && sudo apt upgrade -y
```
Temel paketleri yüklüyoruz.
```
sudo apt install git curl tar wget libssl-dev jq build-essential gcc make
```
add-apt-repository paketini Yüklüyoruz
```
sudo apt update
sudo apt install software-properties-common
sudo apt update
```
Go Yüklüyoruz
```
sudo add-apt-repository ppa:longsleep/golang-backports
sudo apt update
sudo apt install golang-go
```
Gerekli ayarları yapıyoruz.
```
echo "export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> $HOME/.profile
source $HOME/.profile
```
Go versiyonu kontrol ediyoruz, v1.21 veya üzeri olmalı.
```
go version
```
Fairblock node'un eski bir versiyonu kurulu ise aşağıdaki komutlarla kaldırıyoruz ve güncel repoyu indiriyoruz.
```
cd $HOME
rm -rf fairyring
git clone https://github.com/Fairblock/fairyring.git
cd fairyring
```
