Persaud: Open-Source AI Agent on Solana

Persaud is an open-source AI agent designed to deliver real-time Solana data, AI-powered interactions, wallet integration, and developer-friendly features. It leverages cutting-edge AI technologies like GPT-4 to provide an intelligent and interactive experience for blockchain users and developers.

🚀 Features

Real-time Solana Data

- **Live price tracking and market analysis**
- **Trending token insights**
- **Wallet balance monitoring**
- **Transaction analysis with detailed breakdowns**
- **Jito MEV rewards tracking**
- **Compressed NFT minting**

AI-Powered Interactions

- **Natural language processing via GPT-4**
- **Context-aware responses**
- **Blockchain-specific knowledge integration**
- **Sarcastic personality traits**
- **Custom function calling**

Wallet Integration

- **Built-in agent wallet functionality**
- **Secure SOL transfers**
- **Transaction validation**
- **Balance management**
- **NFT minting capabilities**

Developer Experience

- **TypeScript support**
- **Hot reload development**
- **Comprehensive API documentation**
- **Rate limiting protection**
- **Error handling with personality**

Third-Party Integrations

- **Helius RPC integration**
- **Crossmint NFT minting**
- **Jito MEV analytics**
- **CoinGecko price feeds**
- **Jupiter Swap**
- **Birdeye API**

Multi-Platform Support

- **Telegram bot integration**
- **Cross-platform message syncing**
- **Real-time notifications**
- **Command-based interactions**
- **Inline keyboard support**

⚙️ Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/), [yarn](https://yarnpkg.com/), [pnpm](https://pnpm.io/), or [bun](https://bun.sh/)

🛠 Environment Setup

Create a .env.local file in the root directory.

Add the following environment variables:

NEXT_PUBLIC_HELIUS_API_KEY=your_helius_api_key
WALLET_MNEMONIC=your_wallet_mnemonic
CROSSMINT_API_KEY=your_crossmint_api_key
CROSSMINT_COLLECTION_ID=your_crossmint_collection_id
NEXT_PUBLIC_QUICKNODE_RPC_URL=your_quicknode_rpc_url # optional backup for helius
NEXT_PUBLIC_BIRDEYE_API_KEY=your_birdeye_api_key
TELEGRAM_BOT_TOKEN=your_telegram_bot_token
TELEGRAM_WEBHOOK_URL=your_webhook_url # Optional: for production deployments
OPENAI_API_KEY=your_openai_key
BOT_API_BASE_URL=http://127.0.0.1:3000 # if running locally

🚀 Getting Started

Clone the repository:

git clone https://github.com/Persaudoing/persaud.git
cd persaud

Install dependencies:

npm install
# or
yarn install
# or
pnpm install
# or
bun install

Run the development server:

npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev

Open http://localhost:3000 to see the result.

📂 Project Structure

├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── birdeye/
│   │   │       └── trending/
│   │   │           └── route.ts
│   │   │   └── crossmint/
│   │   │       └── route.ts
│   │   │   └── wallet/
│   │   │       └── balance/
│   │   │           └── route.ts
│   │   │       └── send/
│   │   │           └── route.ts
│   │   │   └── lulo/
│   │   │       └── rates/
│   │   │           └── route.ts
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── Chat.tsx
│   │   └── ApiKeyModal.tsx
│   └── utils/
│       ├── wallet.ts
│       ├── helius.ts
│       ├── coingecko.ts
│       ├── validation.ts
│       ├── jito.ts
│       └── openai.ts
│       └── jup.ts
│       └── birdeye.ts
│       └── lulo.ts
├── public/
│   └── assets/
├── types/
│   └── index.ts
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── package.json

📡 API Routes

POST /api/crossmint

- **Mint compressed NFTs**
- **Parameters:**
  - `recipient: string`
  - `name: string`
  - `image: string`
  - `description: string`
- **Returns:** NFT minting response

GET /api/wallet/balance

- **Get wallet balance**
- **Returns:** Balance in SOL and USD

POST /api/wallet/send

- **Send SOL to address**
- **Parameters:**
  - `recipient: string`
  - `amount: number`
- **Returns:** Transaction signature

GET /api/birdeye/trending

- **Get trending tokens from Birdeye**
- **Parameters:**
  - `limit: number` (default: 10)
- **Returns:** List of trending tokens

GET /api/lulo/rates

- **Get current USDC lending rates across Solana protocols**
- **Returns:** List of lending rates

🤖 AI-Powered Capabilities

Persaud integrates advanced AI features powered by GPT-4:
- **Natural language understanding:** Enables context-aware interactions.
- **Customizable personality:** Create a unique user experience with sarcasm or other traits.
- **Blockchain insights:** AI capabilities fine-tuned for Solana and decentralized ecosystems.

📜 License

This project is licensed under the MIT License. See the LICENSE file for details.

Happy building with Persaud! 🌟
