# TestRail: Native API Reference

A consolidated summary of TestRail's API configuration, with links to official documentation.

- **Official docs:** https://support.testrail.com/hc/en-us/sections/7077185274644-API-reference
- **API base URL:** `{instanceUrl}/index.php?/api/v2`

## Authentication

### Basic Authentication

HTTP Basic authentication using the TestRail account email as the username and the TestRail API key as the password, plus the tenant instance URL.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Instance URL:** `instanceUrl` · required · Your TestRail instance base URL without a trailing slash, for example https://example.testrail.io

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.testrail.com/hc/en-us/articles/7077039051284-Accessing-the-API)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
