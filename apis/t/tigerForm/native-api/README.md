# Tiger Form: Native API Reference

A consolidated summary of Tiger Form's API configuration, with links to official documentation.

- **Official docs:** https://tigerform.helpscoutdocs.com/article/249-connect-tiger-form-with-other-applications
- **API base URL:** `https://form-qr-code-generator.com`

## Authentication

### API Key

Connect Tiger Form with an API key from Settings > Advanced Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tigerform.helpscoutdocs.com/article/249-connect-tiger-form-with-other-applications)

## API conventions

Responses from this API use JSON.
