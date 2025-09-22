# Microsoft MCP Workshop

[Your First Real MCP Project – Hands-On Workshop](https://www.meetup.com/azure-usergroup-denmark/events/310761349)
Date: 2025-09-22

## Part-1 Main concepts

Speaker: Nikos Delis

https://github.com/nikosdelis/mcp-ws

1. Server - Tools, Resources, Prompts
2. Host (Orchestrator) - VS Code
3. Client - Inspector; GitHub Copilot

### What's the catch?

- Security: Someone sends a webpage with malicious code that commands the agent to do bad things!
- Performance: tokens and hallucinations

### Workshop commands

```bash
dotnet new console
dotnet add package Microsoft.Extensions.Hosting
dotnet add package ModelContextProtocol --prerelease
dotnet build
dotnet run
```

```bash
npx @modelcontextprotocol/inspector dotnet run
```

## Part 2 - Governance and Policies

Speaker:

MCP servers to enable AI Agents.
Expose the API as MCP Server in API Management.
The operations can be exposed as tools.

Make sure there is Standard OpenAPI documentation (OpenAPI Specification (OAS)) for better LLM interaction.

### OpenAPI Documentation

This is really important for the LLM to find the right MCP tool.

### MCP Governance with Azure API Management

[Secure access to MCP servers in API Management](https://learn.microsoft.com/en-us/azure/api-management/secure-mcp-servers)

```json
{
  "name": "My MCP Server",
  "type": "remote",
  "url": "https://my-api-management-instance.azure-api.net/my-mcp-server",
  "transport": "streamable-http",
  "headers": {
    "Ocp-Apim-Subscription-Key": "<subscription-key>"
  }
}
```

### Open API Standard Documentation

Note: Not any REST API
