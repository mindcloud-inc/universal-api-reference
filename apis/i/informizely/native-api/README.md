# Informizely: Native API Reference

A consolidated summary of Informizely's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://www.informizely.com/help/report-api
- **API base URL:** `https://api.informizely.com/api/v1`

## Authentication

### Basic Auth

Use your Informizely API Key as the username and your API Secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.informizely.com/help/report-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `text/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get All Survey Data](actions/get-all-survey-data.md) | `GET /all` | [docs](https://www.informizely.com/help/report-api) |
| [Get Response Count](actions/get-response-count.md) | `GET /count` | [docs](https://www.informizely.com/help/report-api) |
| [Get Survey Stats](actions/get-survey-stats.md) | `GET /stats` | [docs](https://www.informizely.com/help/report-api) |
| [List Questions](actions/list-questions.md) | `GET /questions` | [docs](https://www.informizely.com/help/report-api) |
| [List Responses](actions/list-responses.md) | `GET /responses` | [docs](https://www.informizely.com/help/report-api) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://www.informizely.com/help/report-api) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://www.informizely.com/help/report-api) |
