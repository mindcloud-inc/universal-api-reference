# Triggerbee: Native API Reference

A consolidated summary of Triggerbee's API configuration, with links to official documentation.

- **Official docs:** https://help.triggerbee.com/en/collections/12371733-developer-resources
- **API base URL:** `https://api-gw.triggerbee.com`

## Authentication

### API Key

Use a Triggerbee API key created in Account and customizations > Developer. The API key authenticates webhook-style Triggerbee routes; current public docs do not expose a broad admin API catalog.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://help.triggerbee.com/en/articles/11069746-integrating-with-centra)
