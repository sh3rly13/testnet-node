# Mac cihazınızda 2 dk işlem ile rolleri alın
>[!NOTE]
>Gereklilikler : Base üzerinde 1 USDC  - 0.0002 ETH - infura RPC - Mac (apple) bilgisayar
<details><summary>Yardım Aldığım Kişiler</summary>

- [Himess](https://github.com/Himess/Boundless-Dev-Prover-Rol-Alma)
- [HerculesNode](https://github.com/HerculesNode/Testnet-Rehber/blob/main/Boundless/boundless-role.md)
  
</details>

## KURULUM 
>[!NOTE]
>Komutları tek tek (satır satır) çalıştırınız.

```zsh
brew update
brew upgrade
```
```zsh
brew install curl git gcc make cmake protobuf
```
```zsh
screen -S boundless
```
```zsh
git clone https://github.com/boundless-xyz/boundless
```
```zsh
cd boundless
```
```zsh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```zsh
source $HOME/.cargo/env
```
```zsh
curl -L https://risczero.com/install | bash
```
```zsh
restart your shell or run kısmındaki kodu çalıştırın  rzup install
```
```zsh
cargo install --git https://github.com/risc0/risc0 bento-client --bin bento_cli  export PATH="$HOME/.cargo/bin:$PATH"
```
```zsh
echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc
```
```zsh
source ~/.bashrc  cargo install --locked boundless-cli
```
```zsh
nano .env.base
```
### Şimdi infura Rpc almamız gerek [Infura](https://developer.metamask.io)


