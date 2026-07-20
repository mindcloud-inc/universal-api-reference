# Online-Convert: Native API Reference

A consolidated summary of Online-Convert's API configuration, with links to official documentation.

- **Official docs:** https://www.api2convert.com/documentation
- **OpenAPI specification:** https://api.api2convert.com/v2/schema
- **API base URL:** `https://api.api2convert.com`

## Authentication

### API Key

Authenticate with an Online-Convert API key sent in the X-Oc-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Oc-Api-Key: <apiKey>
```

[Official authentication documentation](https://www.api2convert.com/documentation/getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.
