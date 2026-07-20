# CrewAI: Native API Reference

A consolidated summary of CrewAI's API configuration, with links to official documentation.

- **Official docs:** https://docs.crewai.com/en/api-reference/introduction
- **API base URL:** `{baseUrl}`

## Authentication

### Bearer Token

### Credentials

- **API Key:** `apiKey` · required
- **Base URL:** `baseUrl` · required · Deployed CrewAI crew URL, for example https://your-crew-name.crewai.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.crewai.com/en/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `inputs`.
