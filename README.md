# Genesis DB MCP Server (Preview)

**Preview Release:** This is an early version of the Genesis DB MCP Server. Features and API structure may change before the stable 1.0 release.

A Model Context Protocol (MCP) server that provides AI clients access to Genesis DB events. This server enables natural language queries against your Genesis DB instance, allowing questions like "How many users are in the system?" or "How many orders did we have last week?"

## Installation

### Download the MCP Server

[Download Genesis DB MCP Server (Preview): macOS (Apple Silicon)](https://raw.githubusercontent.com/genesisdb-io/genesisdb-io-mcp-server/main/build/0.0.1/darwin/arm64/genesisdb-io-mcp-server-0.0.1-darwin-arm64.tar.gz)

[Download Genesis DB MCP Server (Preview): macOS (Intel)](https://raw.githubusercontent.com/genesisdb-io/genesisdb-io-mcp-server/main/build/0.0.1/darwin/amd64/genesisdb-io-mcp-server-0.0.1-darwin-amd64.tar.gz)

[Download Genesis DB MCP Server (Preview): Linux (AMD64)](https://raw.githubusercontent.com/genesisdb-io/genesisdb-io-mcp-server/main/build/0.0.1/linux/amd64/genesisdb-io-mcp-server-0.0.1-linux-amd64.tar.gz)

[Download Genesis DB MCP Server (Preview): Linux (ARM64)](https://raw.githubusercontent.com/genesisdb-io/genesisdb-io-mcp-server/main/build/0.0.1/linux/arm64/genesisdb-io-mcp-server-0.0.1-linux-arm64.tar.gz)


### Configuring with Claude Desktop

Add this server to your Claude Desktop configuration file:

**macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "genesisdb": {
      "command": "/path/to/genesisdb-mcp-server",
      "env": {
        "GENESISDB_HOST": "http://localhost:8080",
        "GENESISDB_AUTH_TOKEN": "your-bearer-token"
      }
    }
  }
}
```

## Example Queries

Once configured with an AI client, you can ask questions like:

- "Wie viele Benutzer sind im System angemeldet?" (How many users are logged into the system?)
- "Wie viele Bestellungen hatten wir in der Vorwoche?" (How many orders did we have last week?)
- "Zeige mir alle Events für Kunde XYZ" (Show me all events for customer XYZ)
- "Welche Event-Typen gibt es in der Datenbank?" (What event types exist in the database?)

## Features

- **Query Events**: Search events by type, time range, and subject pattern
- **Count Events**: Get event counts grouped by type
- **List Event Types**: Discover all available event types in your database
- **Get Events by Subject**: Retrieve all events for a specific entity/subject

## License

MIT

## Author

* E-Mail: mail@genesisdb.io
* URL: https://www.genesisdb.io
* Docs: https://docs.genesisdb.io
