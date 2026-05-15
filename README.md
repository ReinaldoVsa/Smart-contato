# 🔮 Smart Asset Wallet PWA

**Saque, transferência e troca de ativos blockchain — 100% no navegador, mobile-first PWA.**

## ✨ Funcionalidades

- 🔗 **WalletConnect v2** — assine transações com qualquer carteira compatível (MetaMask, Trust, Coinbase, Rainbow...)
- 🏦 **Saque de ativos** — ETH/nativo, tokens ERC-20, chamadas diretas em contratos inteligentes
- ➡️ **Transferência** — tokens nativos, ERC-20 e NFTs (ERC-721)
- ⇄ **Swap de tokens** — via DEX Uniswap V2-compatível (Uniswap, QuickSwap, PancakeSwap...)
- 📜 **Smart Contract** — carregue qualquer contrato ERC-20 e consulte saldo
- ⚡ **Alchemy** — integração para RPC confiável e histórico de transações
- 📋 **Histórico** — transações persistidas localmente com link para o explorer
- 📱 **PWA installable** — instale no celular como app nativo
- 🌐 **Multi-chain** — Ethereum, Polygon, BNB Chain, Arbitrum, Optimism, Base, Avalanche

## 🚀 Deploy no GitHub Pages

### 1. Crie o repositório
```bash
git init
git add .
git commit -m "chore: initial smart wallet PWA"
git branch -M main
git remote add origin https://github.com/SEU_USER/smart-asset-wallet.git
git push -u origin main
```

### 2. Habilite GitHub Pages
- Acesse: `Settings → Pages`
- Source: **GitHub Actions**
- O workflow `.github/workflows/deploy.yml` faz o deploy automático

### 3. Acesse
```
https://SEU_USER.github.io/smart-asset-wallet/
```

## ⚙️ Configuração

Abra o app → botão ⚙ (canto superior direito) e insira:

| Campo | Como obter |
|-------|-----------|
| **Alchemy API Key** | [alchemy.com](https://www.alchemy.com) → Create App → copie a API Key |
| **WalletConnect Project ID** | [cloud.walletconnect.com](https://cloud.walletconnect.com) → New Project → copie o Project ID |

## 🔗 Redes Suportadas

| Rede | Chain ID | DEX |
|------|----------|-----|
| Ethereum Mainnet | 1 | Uniswap V2 |
| Polygon | 137 | QuickSwap |
| BNB Chain | 56 | PancakeSwap |
| Arbitrum One | 42161 | SushiSwap |
| Optimism | 10 | Velodrome |
| Base | 8453 | BaseSwap |
| Avalanche | 43114 | — |

## 🛡️ Segurança

- **Nenhuma chave privada armazenada** — transações assinadas via WalletConnect na sua carteira
- Modo leitura disponível com endereço manual (sem transações)
- Confirmação de transação antes de cada envio
- Dados locais somente no seu dispositivo (localStorage)

## 📁 Estrutura

```
smart-asset-wallet/
├── index.html          # App principal
├── manifest.json       # PWA manifest
├── sw.js               # Service Worker (offline)
├── css/
│   └── style.css       # Estilos
├── js/
│   ├── config.js       # Constantes e redes
│   ├── alchemy.js      # Integração Alchemy/RPC
│   ├── wallet.js       # WalletConnect + conexão
│   ├── contract.js     # Interação com contratos
│   ├── transactions.js # Saque e transferência
│   ├── swap.js         # Swap DEX
│   ├── ui.js           # Helpers de UI
│   └── app.js          # Init e event handlers
├── icons/              # Ícones PWA
└── .github/
    └── workflows/
        └── deploy.yml  # CI/CD GitHub Actions
```

## 🧰 Tecnologias

- **ethers.js v5** — interação com contratos e carteiras
- **WalletConnect v2** — assinatura de transações
- **Alchemy** — RPC confiável e APIs avançadas
- **Uniswap V2 Router** — swap de tokens
- **Vanilla JS + CSS** — zero frameworks, máxima compatibilidade

## 📝 Licença

MIT — uso livre.
