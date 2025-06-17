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


`brew update`
`brew upgrade`

```zsh
brew update
brew upgrade

brew install curl git gcc make cmake protobuf

screen -S boundless

git clone https://github.com/boundless-xyz/boundless

cd boundless

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

source $HOME/.cargo/env

curl -L https://risczero.com/install | bash

restart your shell or run kısmındaki kodu çalıştırın  rzup install

cargo install --git https://github.com/risc0/risc0 bento-client --bin bento_cli  export PATH="$HOME/.cargo/bin:$PATH"

echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc

source ~/.bashrc  cargo install --locked boundless-cli

nano .env.base
```
### Şimdi infura Rpc almamız gerek [Infura](https://developer.metamask.io)


