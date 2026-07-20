# SignPath: Native API Reference

A consolidated summary of SignPath's API configuration, with links to official documentation.

- **Official docs:** https://docs.signpath.io/build-system-integration
- **OpenAPI specification:** https://app.signpath.io/api/swagger/v1/swagger.json
- **API base URL:** `https://app.signpath.io/api/v1/{organizationId}`

## Authentication

### API token

Authenticate to SignPath with a bearer API token.

### Credentials

- **API Key:** `apiKey` · required
- **Organization ID:** `organizationId` · required · SignPath organization UUID used in API paths.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.signpath.io/build-system-integration)

## API conventions

Responses from this API use JSON.
