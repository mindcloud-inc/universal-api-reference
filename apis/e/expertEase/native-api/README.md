# ExpertEase: Native API Reference

A consolidated summary of ExpertEase's API configuration.

- **OpenAPI specification:** https://backend.experteaseai.com/api/schema/
- **API base URL:** `https://backend.experteaseai.com`

## Authentication

### Token API Key

Use an ExpertEase API key sent as Authorization: Token <apiKey>.

### Credentials

- **API Key:** `apiKey` · required · Your ExpertEase API key. MindCloud sends it as Authorization: Token <apiKey>.

[Official authentication documentation](https://docs.experteaseai.com/api-key-how-to-use-expertease-ai-api-key.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
