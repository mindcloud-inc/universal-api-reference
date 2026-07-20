# Wufoo: Native API Reference

A consolidated summary of Wufoo's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://wufoo.github.io/docs/
- **API base URL:** `https://{subdomain}.wufoo.com/api/v3`

## Authentication

### Basic Auth

Use your Wufoo API key as the Basic Auth username, plus any non-empty password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Account Subdomain:** `subdomain` · required · The Wufoo account subdomain used to build API URLs, for example `mindcloudapps`.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://wufoo.github.io/docs/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Form Comments](actions/count-form-comments.md) | `GET /forms/:identifier/comments/count.json` | [docs](https://wufoo.github.io/docs/#forms) |
| [Count Form Entries](actions/count-form-entries.md) | `GET /forms/:identifier/entries/count.json` | [docs](https://wufoo.github.io/docs/#entries) |
| [Count Report Entries](actions/count-report-entries.md) | `GET /reports/:identifier/entries/count.json` | [docs](https://wufoo.github.io/docs/#reports) |
| [Get Form](actions/get-form.md) | `GET /forms/:identifier.json` | [docs](https://wufoo.github.io/docs/#forms) |
| [Get Report](actions/get-report.md) | `GET /reports/:identifier.json` | [docs](https://wufoo.github.io/docs/#reports) |
| [List Form Comments](actions/list-form-comments.md) | `GET /forms/:identifier/comments.json` | [docs](https://wufoo.github.io/docs/#forms) |
| [List Form Entries](actions/list-form-entries.md) | `GET /forms/:identifier/entries.json` | [docs](https://wufoo.github.io/docs/#entries) |
| [List Form Fields](actions/list-form-fields.md) | `GET /forms/:identifier/fields.json` | [docs](https://wufoo.github.io/docs/#forms) |
| [List Forms](actions/list-forms.md) | `GET /forms.json` | [docs](https://wufoo.github.io/docs/#forms) |
| [List Report Entries](actions/list-report-entries.md) | `GET /reports/:identifier/entries.json` | [docs](https://wufoo.github.io/docs/#reports) |
| [List Report Fields](actions/list-report-fields.md) | `GET /reports/:identifier/fields.json` | [docs](https://wufoo.github.io/docs/#reports) |
| [List Report Widgets](actions/list-report-widgets.md) | `GET /reports/:identifier/widgets.json` | [docs](https://wufoo.github.io/docs/#reports) |
| [List Reports](actions/list-reports.md) | `GET /reports.json` | [docs](https://wufoo.github.io/docs/#reports) |
| [List Users](actions/list-users.md) | `GET /users.json` | [docs](https://wufoo.github.io/docs/#users) |
| [Submit Form Entry](actions/submit-form-entry.md) | `POST /forms/:identifier/entries.json` | [docs](https://wufoo.github.io/docs/#entries) |
