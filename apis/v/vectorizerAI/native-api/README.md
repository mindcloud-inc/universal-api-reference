# Vectorizer AI: Native API Reference

A consolidated summary of Vectorizer AI's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://vectorizer.ai/api
- **API base URL:** `https://api.vectorizer.ai/api/v1`

## Authentication

### API Credentials

HTTP Basic authentication using the Vectorizer API Id as the username and API Secret as the password.

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

[Official authentication documentation](https://vectorizer.ai/api)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Account Status](actions/account-status.md) | `GET /account` | [docs](https://vectorizer.ai/api) |
| [Delete](actions/delete.md) | `POST /delete` | [docs](https://vectorizer.ai/api) |
| [Download](actions/download.md) | `POST /download` | [docs](https://vectorizer.ai/api) |
| [Vectorize](actions/vectorize.md) | `POST /vectorize` | [docs](https://vectorizer.ai/api) |
