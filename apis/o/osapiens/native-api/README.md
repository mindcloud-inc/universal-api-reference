# Osapiens: Native API Reference

A consolidated summary of Osapiens's API configuration.

- **API base URL:** `https://{environment}`

## Authentication

### Basic Auth

Basic authentication for the osapiens T&T endpoint.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Environment:** `environment` · required · Environment host. Use qa.osapiens.cloud for Sandbox/QA. Replace with the production host once Osapiens confirms it.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://qa.osapiens.cloud/data/in/rest/e2e-testing-ttos-1/tpd/capture-json/)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml;charset=UTF-8` |
