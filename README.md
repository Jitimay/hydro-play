# HydroPlay: Decentralized Water Broker for Rural Africa

**"Turning DeFi into Drinkable Water"**

## Overview
HydroPlay transforms crypto payments into real-world water access for rural communities with limited connectivity. Using blockchain transactions on basic 2G networks, villagers can buy clean water through transparent, corruption-free distribution.

## Architecture
- **Blockchain (Base L2)**: Processes payments
- **AI Bridge (Python)**: Listens to blockchain events, generates SMS commands
- **ESP32 (LilyGO T-Call SIM800L)**: Receives 1-5 byte commands to activate pumps

## Quick Start

### Prerequisites
- Node.js 18+
- Python 3.8+
- Arduino IDE
- Base testnet wallet

### Setup

1. **Clone Repository**:
```bash
git clone https://github.com/yourusername/hydroplay.git
cd hydroplay
```

2. **Environment Configuration**:
```bash
# Copy example environment files
cp src/blockchain/.env.example src/blockchain/.env
cp src/ai-bridge/.env.example src/ai-bridge/.env
# Edit .env files with your configuration
```

3. **Smart Contract Deployment**:
```bash
cd src/blockchain
npm install
npx hardhat deploy --network base-sepolia
```

4. **AI Bridge Setup**:
```bash
cd src/ai-bridge
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

5. **ESP32 Setup**:
- Flash `src/esp32/water_pump.ino` to LilyGO T-Call
- Configure SIM card and pump GPIO pins

6. **Web Interface**:
```bash
cd src/web
# Serve files using any HTTP server
python -m http.server 8000
```

## Testing in Production (TIP)

1. **Test Payment Flow**:
   - Connect wallet to Base testnet
   - Purchase water credits via web interface
   - Verify SMS command sent to ESP32

2. **Hardware Test**:
   - Send test SMS to ESP32
   - Confirm pump activation
   - Check water flow sensor readings

## Use Cases
- Community water kiosks
- NGO deployment
- Disaster relief
- Rural water access

## Impact
Provides transparent, automated, corruption-free clean water distribution for rural Africa.

## Built with Vibe Coding
This project extensively uses AI-assisted development. See `prompts.md` and `ai_logs/` for detailed documentation of the AI development process.
# HydroPlay-DeFi-Water-Access-
# hydro-play
