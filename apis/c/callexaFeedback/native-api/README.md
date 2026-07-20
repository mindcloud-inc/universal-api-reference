# Callexa Feedback: Native API Reference

A consolidated summary of Callexa Feedback's API configuration, with links to official documentation.

- **Official docs:** https://www.callexa.com/api/doc/index.html
- **API base URL:** `https://www.callexa.com/api/v2`

## Authentication

### Basic Auth

Authenticate with your Callexa login email as the username and your API key as the password over HTTPS Basic Auth.

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

[Official authentication documentation](https://www.callexa.com/api/doc/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
