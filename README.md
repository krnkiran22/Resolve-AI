# ResolveAI - Decentralized Web3 Dispute Resolution Platform

<div align="center">
  <img src="https://img.shields.io/badge/React-19.0-blue?style=for-the-badge&logo=react" alt="React">
  <img src="https://img.shields.io/badge/Solidity-0.8.19-purple?style=for-the-badge&logo=solidity" alt="Solidity">
  <img src="https://img.shields.io/badge/Powered%20by-Groq%20AI-green?style=for-the-badge" alt="Groq AI">
  <img src="https://img.shields.io/badge/Blockchain-Monad%20Testnet-orange?style=for-the-badge" alt="Monad">
</div>

## 🚀 Problem Statement

### The Challenge
In the rapidly expanding Web3 ecosystem, users frequently encounter disputes related to:
- **Failed Transactions**: Gas failures, reverted transactions, and contract errors
- **NFT Trading Issues**: Fake collections, metadata problems, and marketplace disputes
- **DeFi Protocol Problems**: Yield farming failures, liquidity issues, and smart contract bugs
- **Cross-chain Bridge Failures**: Stuck tokens and failed cross-chain transfers

### Current Pain Points
1. **Lack of Automated Analysis**: Users struggle to understand complex transaction failures
2. **No Centralized Resolution**: Disputes are scattered across multiple platforms
3. **Limited AI Integration**: Existing solutions lack intelligent transaction analysis
4. **Poor User Experience**: Technical barriers prevent non-technical users from resolving disputes
5. **Inefficient Juror System**: No streamlined process for dispute review and resolution

### Our Solution: ResolveAI
ResolveAI is a comprehensive decentralized dispute resolution platform that combines:
- **AI-Powered Analysis**: Groq's Llama3-70B model for intelligent transaction investigation
- **Smart Contract Integration**: Automated dispute submission and juror decision system
- **User-Friendly Interface**: Intuitive chat-based dispute resolution workflow
- **Blockchain Transparency**: All disputes and resolutions recorded on-chain
- **Expert Juror Network**: Authorized jurors for fair and informed dispute resolution

## 🎯 Key Features

### 🤖 AI-Powered Dispute Analysis
- **Intelligent Chat Interface**: Natural language interaction for dispute submission
- **Automatic Transaction Analysis**: Real-time blockchain data fetching and interpretation
- **Smart Recommendations**: AI-generated refund decisions (Full/Partial/No Refund/Not Possible)
- **Context-Aware Responses**: Conversation history and transaction context integration

### ⛓️ Blockchain Integration
- **Smart Contract System**: Automated dispute management on Monad testnet
- **Two-Step Submission**: Optimized contract design to avoid stack depth errors
- **Event-Driven Architecture**: Real-time updates through blockchain events
- **IPFS Evidence Storage**: Decentralized storage for dispute evidence via Pinata

### 👨‍⚖️ Juror Management System
- **Authorized Juror Network**: Owner-controlled juror authorization system
- **Challenge Mechanism**: Users can challenge AI decisions for human review
- **Comprehensive Review Interface**: Detailed dispute information for informed decisions
- **Transparent Resolution**: All decisions recorded on-chain with reasoning

### 🎨 Modern User Experience
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Real-time Updates**: Live chat interface with WebSocket integration
- **Custom Theming**: Unique RGB(85, 255, 225) accent color scheme
- **Intuitive Navigation**: Multi-page application with React Router

## 🛠️ Technologies Used

### Frontend Stack
- **React 19** with TypeScript for type safety
- **Vite** for fast development and building
- **Tailwind CSS** for responsive styling
- **React Router** for navigation
- **React Toastify** for notifications

### Blockchain & Web3
- **Solidity 0.8.19** for smart contracts
- **ethers.js** for blockchain interaction
- **MetaMask** integration for wallet connectivity
- **Monad Testnet** for deployment

### AI & External Services
- **Groq API** with Llama3-70B model
- **Pinata IPFS** for decentralized storage
- **WebSocket** for real-time communication

### Development Tools
- **ESLint** for code quality
- **TypeScript** for type checking
- **Git** for version control

## 📋 Installation & Setup

### Prerequisites
- Node.js 16+ and npm
- MetaMask browser extension
- Git for version control

### 1. Clone Repository
```bash
git clone https://github.com/krnkiran22/Resolve-AI.git
cd Resolve-AI
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Configuration
Create a `.env` file in the root directory:
```env
VITE_GROQ_API_KEY=your_groq_api_key_here
VITE_PINATA_API_KEY=your_pinata_api_key_here
VITE_PINATA_SECRET_KEY=your_pinata_secret_key_here
```

### 4. Get API Keys

#### Groq API Key:
1. Visit [Groq Console](https://console.groq.com)
2. Create account and generate API key
3. Add to `.env` file

#### Pinata IPFS Keys:
1. Visit [Pinata](https://pinata.cloud)
2. Create account and get API keys
3. Add both API key and secret to `.env`

### 5. Smart Contract Deployment

#### Option 1: Use Existing Contract
The contract is already deployed on Monad testnet. Update the contract address in:
- `src/components/DisputePage.tsx`
- `src/pages/JurorPage.tsx`

#### Option 2: Deploy Your Own
1. Open [Remix IDE](https://remix.ethereum.org/)
2. Copy contract from `contracts/MonadContract.sol`
3. Compile with Solidity 0.8.19+
4. Deploy to Monad testnet via MetaMask
5. Update contract addresses in frontend files

### 6. Development Server
```bash
npm run dev
```
Application will be available at `http://localhost:5173`

### 7. Production Build
```bash
npm run build
npm run preview
```

## 🌐 Network Configuration

### Monad Testnet Setup
Add Monad testnet to MetaMask:
- **Network Name**: Monad Testnet
- **RPC URL**: `https://testnet1.monad.xyz`
- **Chain ID**: `41454`
- **Currency Symbol**: `MON`
- **Block Explorer**: `https://testnet1.monad.xyz`

## 📱 Application Structure

```
src/
├── components/
│   ├── ChatInterface.tsx     # AI chat interface
│   └── DisputePage.tsx       # Dispute submission form
├── pages/
│   ├── HomePage.tsx          # Landing page
│   ├── ChatPage.tsx          # AI chat page
│   ├── DashboardPage.tsx     # User dashboard
│   ├── ResolutionPage.tsx    # Dispute resolution
│   ├── JurorPage.tsx         # Juror review interface
│   └── HelpPage.tsx          # Help and documentation
├── router/
│   └── AppRouter.tsx         # Application routing
├── utils/
│   ├── aiAgent.ts            # Groq AI integration
│   ├── alithClient.ts        # AI client utilities
│   └── blockchain.ts         # Blockchain utilities
└── contracts/
    ├── DisputeResolution.sol # Full dispute contract
    └── MonadContract.sol     # Simplified test contract
```

## 🔄 User Workflow

### 1. Dispute Submission
1. User describes their issue in the chat interface
2. AI analyzes the problem and requests transaction details
3. System automatically fetches blockchain data
4. AI provides initial recommendation
5. Dispute is submitted to smart contract with IPFS evidence

### 2. Challenge Process
1. User can challenge AI decision if unsatisfied
2. Dispute status changes to "Challenged"
3. Authorized jurors can see challenged disputes
4. Human review process begins

### 3. Juror Review
1. Authorized jurors access JurorPage
2. View all challenged disputes with full context
3. Analyze AI recommendations and evidence
4. Submit final decision with reasoning
5. Resolution recorded on-chain

## 🎮 Demo & Testing

### Test the Application
1. Visit the deployed application
2. Connect MetaMask wallet to Monad testnet
3. Submit a test dispute with transaction hash
4. Challenge the AI decision
5. Review as an authorized juror (if authorized)

### Sample Test Data
```
Transaction Hash: 0x123...abc (any valid format)
Description: "My NFT purchase failed but gas was deducted"
Contract Address: 0x456...def
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Groq** for providing fast AI inference
- **Monad** for the testnet infrastructure
- **Pinata** for IPFS storage services
- **OpenZeppelin** for smart contract security patterns

## 📞 Support & Contact

- **GitHub Issues**: [Report bugs or request features](https://github.com/krnkiran22/Resolve-AI/issues)
- **Documentation**: Check the `/docs` folder for detailed guides
- **Community**: Join our discussions in GitHub Discussions

---

<div align="center">
  <p><strong>Built with ❤️ for the Web3 community</strong></p>
  <p>Empowering users with AI-driven dispute resolution on blockchain</p>
</div>
     ```env
     REACT_APP_GROQ_API_KEY=your_groq_api_key_here
     ```

4. **Start the development server**:
   ```bash
   npm run dev
   ```

## Usage

### Basic Chat

1. Open the application in your browser
2. Type your Web3-related questions in the chat input
3. Get AI-powered responses for dispute resolution

### Transaction Analysis

1. Include a transaction hash in your message (e.g., "Analyze this transaction: 0x123...")
2. The system automatically fetches blockchain data from Sepolia
3. AI provides contextualized analysis with transaction details

### Example Queries

- "Analyze this failed NFT trade: 0x123..."
- "Why did my DeFi transaction fail?"
- "Check if this smart contract is legitimate"
- "Investigate suspicious wallet activity"
- "Help me understand this gas fee issue"

## Project Structure

```
src/
├── components/
│   └── ChatInterface.tsx     # Main chat component
├── pages/
│   └── ChatPage.tsx         # Chat page layout
├── utils/
│   ├── aiAgent.ts           # Groq AI integration
│   └── blockchain.ts        # Ethereum/Sepolia integration
└── App.tsx                  # Main application
```

## Key Components

### ChatInterface

- Real-time messaging interface
- Automatic transaction hash detection
- Loading states and animations
- Message history management

### AI Agent

- Groq API integration
- Conversation context management
- Web3-specialized prompts
- Error handling

### Blockchain Service

- Sepolia testnet connection
- Transaction data fetching
- Network status monitoring
- Balance and block queries

## API Integration

The AI agent is configured to use Groq's API:

```typescript
const agent = new Agent({
  model: "llama3-70b-8192",
  apiKey: process.env.REACT_APP_GROQ_API_KEY,
  baseUrl: "https://api.groq.com/openai/v1",
  preamble:
    "You are a helpful AI assistant specializing in Web3 dispute resolution...",
});
```

## Styling

- Custom Tailwind configuration with ResolveAI brand colors
- RGB(85, 255, 225) accent color throughout the interface
- Gradient backgrounds and modern card designs
- Responsive grid layout for desktop and mobile

## Deployment

Build for production:

```bash
npm run build
```

The built files will be in the `dist/` directory, ready for deployment to any static hosting service.

## Environment Variables

- `REACT_APP_GROQ_API_KEY`: Your Groq API key (required)
- `REACT_APP_SEPOLIA_RPC`: Custom Sepolia RPC endpoint (optional)

## License

MIT License - see LICENSE file for details

## Hackathon Notes

This project is designed for rapid deployment in hackathon environments:

- Single-page application with all features in one place
- Environment variables for easy configuration
- Modern tech stack for impressive demos
- Comprehensive error handling for stable presentations
- Mobile-responsive for diverse demo scenarios

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from "eslint-plugin-react-x";
import reactDom from "eslint-plugin-react-dom";

export default tseslint.config([
  globalIgnores(["dist"]),
  {
    files: ["**/*.{ts,tsx}"],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs["recommended-typescript"],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ["./tsconfig.node.json", "./tsconfig.app.json"],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
]);
```
