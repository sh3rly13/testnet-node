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
cargo install --git https://github.com/risc0/risc0 bento-client --bin bento_cli
```
```zsh
export PATH="$HOME/.cargo/bin:$PATH"
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
### Şimdi [Infura](https://developer.metamask.io) Rpc almamız gerek 
Kayıt olun ardından soldaki menüden İnfura Rpc den rpc alın (ücretsiz) Base mainnet in seçili olduğundan emin olun.
Açılan Nano dosyasına aşağıdaki **satırları ekleyin** 
ctrl + x --> y --> enter ile dosyayı kaydedip çıkın
```zsh
export ETH_RPC_URL="ALCHEMY-BASE-MAİNNET-LİNKİ"
export PRIVATE_KEY="CÜZDANINIZIN-PRİVATE-KEYİ" 
```
Aşağıdaki gibi gözükmesi lazım 
```zsh
# Base contract addresses
export VERIFIER_ADDRESS=0x0b144e07a0826182b6b59788c34b32bfa86fb711
export BOUNDLESS_MARKET_ADDRESS=0x26759dbB201aFbA361Bec78E097Aa3942B0b4AB8
export SET_VERIFIER_ADDRESS=0x8C5a8b5cC272Fe2b74D18843CF9C3aCBc952a760

# Public order stream URL
export ORDER_STREAM_URL="https://base-mainnet.beboundless.xyz"
export ETH_RPC_URL="https://base-mainnet.infura.io/v3/xxxxxx"
export PRIVATE_KEY="0x12345..."
```
```zsh
source .env.base
```
Prover Rolü için çalıştırın : Node kurmak istiyorsanız stake 1 kısmını 10 yapın böylelikle 10 USDC stake etmiş oluyorsunuz ve NODE kurabilirsiniz. Ben node kuramayacağım için 1 yaptım.

```zsh
boundless \
  --rpc-url "$ETH_RPC_URL" \
  --private-key "$PRIVATE_KEY" \
  --boundless-market-address 0x26759dbB201aFbA361Bec78E097Aa3942B0b4AB8 \
  --set-verifier-address 0x8C5a8b5cC272Fe2b74D18843CF9C3aCBc952a760 \
  --verifier-router-address 0x0b144e07a0826182b6b59788c34b32bfa86fb711 \
  --order-stream-url "https://base-mainnet.beboundless.xyz" \
  account deposit-stake 1
```

Dev Rolü için çalıştırın : 

```zsh
boundless \
  --rpc-url "$ETH_RPC_URL" \
  --private-key "$PRIVATE_KEY" \
  --boundless-market-address 0x26759dbB201aFbA361Bec78E097Aa3942B0b4AB8 \
  --set-verifier-address 0x8C5a8b5cC272Fe2b74D18843CF9C3aCBc952a760 \
  --verifier-router-address 0x0b144e07a0826182b6b59788c34b32bfa86fb711 \
  --order-stream-url "https://base-mainnet.beboundless.xyz/" \
  account deposit 0.000001
```
### SON 
[GUILD](https://guild.xyz/boundless-xyz)
Guild e Katılın ve yeşilleri gördüyseniz başarılı olmuştur DC den rolleri alın.
<br>
</br>
![](/boundless-prover-dev/dev.png)


