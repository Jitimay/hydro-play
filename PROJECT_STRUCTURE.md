# HydroPlay Project Structure

## Core Components

```
hydro_play/
├── src/
│   ├── blockchain/          # Smart contracts (Solidity)
│   │   ├── contracts/       # WaterBroker.sol
│   │   ├── scripts/         # Deployment scripts
│   │   ├── test/           # Contract tests
│   │   └── hardhat.config.js
│   ├── ai-bridge/          # Python AI service
│   │   ├── main.py         # Main AI bridge server
│   │   ├── requirements.txt # Python dependencies
│   │   └── *.py           # Supporting modules
│   ├── esp32/              # Arduino/ESP32 firmware
│   │   ├── water_pump.ino  # Main pump controller
│   │   └── *.ino          # Additional ESP32 code
│   └── web/                # Frontend interface
│       ├── index.html      # Main UI
│       └── app.js         # Web3 integration
├── tests/                  # Integration tests
├── ai_logs/               # AI development logs
├── docs/                  # Documentation
└── scripts/               # Utility scripts
```

## Key Files

### Smart Contracts
- `src/blockchain/contracts/WaterBroker.sol` - Main water payment contract
- `src/blockchain/hardhat.config.js` - Hardhat configuration for Base L2

### AI Bridge
- `src/ai-bridge/main.py` - Flask server processing SMS payments
- `src/ai-bridge/requirements.txt` - Python dependencies

### Hardware
- `src/esp32/water_pump.ino` - ESP32 pump controller with SMS integration

### Frontend
- `src/web/index.html` - Cyberpunk-themed Web3 interface
- `src/web/app.js` - MetaMask integration and blockchain interaction

## Excluded from Git

- `node_modules/` - NPM dependencies
- `venv/` - Python virtual environments
- `*.db` - SQLite databases
- `*.log` - Log files
- `.env` - Environment variables
- `artifacts/` - Hardhat compilation artifacts
- `cache/` - Build cache files

## Development Setup

1. **Blockchain**: `cd src/blockchain && npm install`
2. **AI Bridge**: `cd src/ai-bridge && pip install -r requirements.txt`
3. **ESP32**: Flash `.ino` files using Arduino IDE
4. **Web**: Serve `src/web/` directory

## Architecture

- **Base L2**: Smart contract deployment
- **Python Flask**: AI bridge service
- **ESP32**: IoT hardware controller
- **Web3**: Frontend blockchain integration
- **SMS**: 2G network communication
