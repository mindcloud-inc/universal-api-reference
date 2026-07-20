# IgnitePost: Native API Reference

A consolidated summary of IgnitePost's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://dashboard.ignitepost.com/api-documentation
- **API base URL:** `https://dashboard.ignitepost.com/api/v1`

## Authentication

### API Key

Connect to IgnitePOST with an API key from Profile > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-TOKEN: <apiKey>
```

[Official authentication documentation](https://dashboard.ignitepost.com/api-documentation)

## API conventions

Response data is read from `data`.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `GET /authenticate` | [docs](https://dashboard.ignitepost.com/api-documentation#authenticate) |
| [Create Order](actions/create-order.md) | `POST /orders` | [docs](https://dashboard.ignitepost.com/api-documentation#create-an-order) |
| [List Default Images](actions/list-default-images.md) | `GET /images` | [docs](https://dashboard.ignitepost.com/api-documentation#list-default-images) |
| [List Fonts](actions/list-fonts.md) | `GET /fonts` | [docs](https://dashboard.ignitepost.com/api-documentation#list-fonts) |
| [List Inserts](actions/list-inserts.md) | `GET /inserts` | [docs](https://dashboard.ignitepost.com/api-documentation#list-inserts) |
| [List Letter Templates](actions/list-letter-templates.md) | `GET /letter_templates` | [docs](https://dashboard.ignitepost.com/api-documentation#list-letter-templates) |
| [Preview Note](actions/preview-note.md) | `POST /preview` | [docs](https://dashboard.ignitepost.com/api-documentation#preview-note) |
| [Retrieve Order](actions/retrieve-order.md) | `GET /orders/:id` | [docs](https://dashboard.ignitepost.com/api-documentation#retrieve-an-order) |
