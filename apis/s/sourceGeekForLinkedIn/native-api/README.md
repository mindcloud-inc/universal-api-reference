# SourceGeek for LinkedIn: Native API Reference

A consolidated summary of SourceGeek for LinkedIn's API configuration, with links to official documentation.

- **Official docs:** https://support.sourcegeek.com/en/articles/12441230-n8n-integration
- **API base URL:** `https://app.sourcegeek.com/api/integrations/n8n/v1`

## Authentication

### API Key

Connect with a SourceGeek API key from Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.sourcegeek.com/en/articles/12441230-n8n-integration)
