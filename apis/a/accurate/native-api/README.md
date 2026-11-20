# Accurate: Native API Reference

A consolidated summary of Accurate's API configuration, with links to official documentation.

- **Official docs:** https://accurate.readme.io/reference
- **API base URL:** `https://api.accuratebackground.com/v3`

## Authentication

### Basic Authentication

Connect using Accurate API credentials.

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

[Official authentication documentation](https://accurate.readme.io/docs/generate-accurate-api-credentials)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.
