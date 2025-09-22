# Microsoft MCP Workshop

2025-09-22

https://www.meetup.com/azure-usergroup-denmark/events/310761349
https://github.com/nikosdelis/mcp-ws

Workshop instructor: Nikos Delis

## Main concepts

1. Server - Tools, Resources, Prompts
2. Host (Orchestrator) - VS Code
3. Client - Inspector; GitHub Copilot

## What's the catch?

- Security: Someone sends a webpage with malicious code that commands the agent to do bad things!
- Performance: tokens and hallucinations

## Workshop commands

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
