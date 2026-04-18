# LinkedIn MCP Server - Setup Instructions

## Prerequisites

- Node.js (v18+)
- npm

## Installation

```bash
npm install
```

## Running the MCP Server

This MCP requires two servers to run simultaneously:
1. **Auth Server** - Handles LinkedIn OAuth authentication
2. **MCP Server** - The main MCP server for LinkedIn integration

### Run Both Servers

Open a new terminal window that starts both the Auth server and MCP server simultaneously:

```powershell
Start-Process powershell -ArgumentList "-NoExit", "-Command", "cd 'C:\Users\Deano\Documents\opencode projects\linkdin_AI\linkedin-mcp'; npx concurrently 'npm run dev:auth' 'npm run dev'"
```

## Configuration

The server runs on:
- **Auth Server**: http://localhost:8000
- **MCP Server**: http://localhost:8001

## Usage

After starting the servers, visit http://localhost:8000/auth/linkedin in your browser to authenticate with LinkedIn.

Once authenticated, use the MCP tools:
- `linkedin-share-post` - Share a text post to LinkedIn
- `linkedin-share-link` - Share a link with commentary to LinkedIn