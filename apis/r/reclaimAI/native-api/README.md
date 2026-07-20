# Reclaim AI: Native API Reference

A consolidated summary of Reclaim AI's API configuration.

- **API base URL:** `https://api.app.reclaim.ai/api`

## Authentication

### API Key

Use a Reclaim API key generated from the Reclaim app settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.reclaim.ai/en/articles/8136585-overview-raycast-extension-for-reclaim-ai)
