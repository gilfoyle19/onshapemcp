# Onshape MCP Server

Enhanced Model Context Protocol (MCP) server for programmatic CAD modeling with Onshape.

## ✨ Features

- **🔍 Document Discovery** - Search and list projects, find Part Studios
- **📐 Parametric Sketching** - Create sketches with rectangles, circles, lines
- **⚙️ Feature Management** - Extrudes, fillets, chamfers, feature trees
- **🔩 Mechanical Components** - Create gears with customizable parameters
- **🎯 Edge Query & Discovery** - Find edges by radius, type, or feature
- **📊 Variable Tables** - Read/write parametric design variables
- **🤖 Full Automation** - Build complete CAD workflows

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- Onshape account with API access

### Setup
```bash
git clone https://github.com/clarsbyte/onshape-mcp.git
cd onshape-mcp
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -e .
```

### Get API Keys
1. Go to [Onshape Developer Portal](https://dev-portal.onshape.com/)
2. Create API key → copy Access Key and Secret Key

### Configure Gemini CLI
Add to your Gemini CLI configuration file (typically `~/.config/gemini-cli/settings.json`):

```json
{
  "mcpServers": {
    "onshape": {
      "command": "/absolute/path/to/onshape-mcp/venv/bin/python",
      "args": ["-m", "onshape_mcp.server"],
      "env": {
        "ONSHAPE_ACCESS_KEY": "your_access_key",
        "ONSHAPE_SECRET_KEY": "your_secret_key"
      }
    }
  }
}
```

### Usage
```bash
onshape-mcp  # Run server
```

Ask Gemini CLI: *"Create a mechanical part with variable dimensions"*"


