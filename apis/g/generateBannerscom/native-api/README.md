# GenerateBanners.com: Native API Reference

A consolidated summary of GenerateBanners.com's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.generatebanners.com/documentation/api
- **API base URL:** `https://api.generatebanners.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Public API Key:** `publicApiKey` · required · Public API key used in the request path segment.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.generatebanners.com/documentation/api)

## API conventions

Responses from this API use JSON. Response data is read from `templates`.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | `GET /{{credentials.publicApiKey}}/template/:id` | [docs](https://www.generatebanners.com/documentation/api) |
| [Get Template Signed URL](actions/get-template-signed-url.md) | `GET /{{credentials.publicApiKey}}/template/:id/sign-url` | [docs](https://www.generatebanners.com/documentation/api) |
| [List Templates](actions/list-templates.md) | `GET /{{credentials.publicApiKey}}/template` | [docs](https://www.generatebanners.com/documentation/api) |
| [Render Template](actions/render-template.md) | `GET /{{credentials.publicApiKey}}/template/:id/render` | [docs](https://www.generatebanners.com/documentation/api) |
