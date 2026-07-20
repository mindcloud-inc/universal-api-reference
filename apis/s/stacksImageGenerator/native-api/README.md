# 88stacks Image Generator: Native API Reference

A consolidated summary of 88stacks Image Generator's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://88stacks.com/docs/1.0.en.html
- **API base URL:** `https://api.88stacks.com`

## Authentication

### API Key

Connect to the 88stacks API with your personal API key from your 88stacks account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://88stacks.com/faq/)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | `POST /api/v1/invokes` | [docs](https://88stacks.com/docs/1.0/invokes/create.en.html) |
| [Create Model](actions/create-model.md) | `POST /api/v1/models` | [docs](https://88stacks.com/docs/1.0/models/create.en.html) |
| [Get Model](actions/get-model.md) | `GET /api/v1/models/:id` | [docs](https://88stacks.com/docs/1.0/models/show.en.html) |
| [List Invokes](actions/list-invokes.md) | `GET /api/v1/invokes` | [docs](https://88stacks.com/docs/1.0/invokes/index.en.html) |
| [List Models](actions/list-models.md) | `GET /api/v1/models` | [docs](https://88stacks.com/docs/1.0/models/index.en.html) |
| [Update Model](actions/update-model.md) | `PATCH /api/v1/models/:id` | [docs](https://88stacks.com/docs/1.0/models/update.en.html) |
