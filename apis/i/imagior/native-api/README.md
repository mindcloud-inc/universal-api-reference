# Imagior: Native API Reference

A consolidated summary of Imagior's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.imagior.com
- **API base URL:** `https://api.imagior.com`

## Authentication

### API Key

Use an Imagior API key with Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.imagior.com/getting-started/first-api-call)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | `POST /image/generate` | [docs](https://docs.imagior.com/api-reference/image-generate) |
| [List All Templates](actions/list-all-templates.md) | `GET /templates/all` | [docs](https://docs.imagior.com/api-reference/retrieve-all-templates) |
| [List Template Elements](actions/list-template-elements.md) | `GET /templates/{templateId}/elements` | [docs](https://docs.imagior.com/api-reference/retrieve-template-elements) |
| [List Template Elements and Their Basic Properties](actions/list-template-elements-and-their-basic-properties.md) | `GET /templates/{templateId}/elements/basic` | [docs](https://docs.imagior.com/api-reference/retrieve-basic-template-elements) |
| [Retrieve Account Details](actions/retrieve-account-details.md) | `GET /user/account` | [docs](https://docs.imagior.com/api-reference/retrieve-account-details) |
