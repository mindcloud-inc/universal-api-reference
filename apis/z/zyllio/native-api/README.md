# Zyllio: Native API Reference

A consolidated summary of Zyllio's API configuration, with links to official documentation.

- **Official docs:** https://www.zyllio.one/api/docs/
- **API base URL:** `https://www.zyllio.one/api/public`

## Authentication

### API key

Connect to the Zyllio Public API with a workspace API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.zyllio.one/api/docs/)
