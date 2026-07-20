# RapidoForm: Native API Reference

A consolidated summary of RapidoForm's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.rapidoform.com/developers/docs/get-started
- **API base URL:** `https://www.rapidoform.com/be`

## Authentication

### API Key

Connect with your RapidoForm API key and account email.

### Credentials

- **API Key:** `apiKey` · required
- **Email:** `email` · required · Registered account email used in RapidoForm API requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.rapidoform.com/developers/docs/create)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /api/survey/create` | [docs](https://www.rapidoform.com/developers/docs/create) |
| [Create Question](actions/create-question.md) | `POST /api/question` | [docs](https://www.rapidoform.com/developers/docs/create) |
| [Create Theme](actions/create-theme.md) | `POST /api/theme` | [docs](https://www.rapidoform.com/developers/docs/create) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/webhook/save` | [docs](https://www.rapidoform.com/developers/docs/webhooks) |
| [List Forms](actions/list-forms.md) | `GET /api/surveys` | [docs](https://www.rapidoform.com/developers/docs/create) |
| [List My Themes](actions/list-my-themes.md) | `GET /api/mytheme` | [docs](https://www.rapidoform.com/developers/docs/create) |
| [List Theme Gallery](actions/list-theme-gallery.md) | `GET /api/theme/gallery` | [docs](https://www.rapidoform.com/developers/docs/create) |
