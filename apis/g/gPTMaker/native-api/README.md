# GPT Maker: Native API Reference

A consolidated summary of GPT Maker's API configuration, with links to official documentation.

- **Official docs:** https://developer.gptmaker.ai/api-reference/introduction
- **OpenAPI specification:** https://developer.gptmaker.ai/api-reference/openapi.json
- **API base URL:** `https://api.gptmaker.ai`

## Authentication

### API Key

Bearer token authentication using a GPT Maker API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.gptmaker.ai/api-reference/introduction)

## API conventions

Responses from this API use JSON.
