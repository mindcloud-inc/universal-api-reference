# WordPress: Native API Reference

A consolidated summary of WordPress's API configuration, with links to official documentation.

- **Official docs:** https://developer.wordpress.org/rest-api/
- **API base URL:** `{siteUrl}/wp-json/wp/v2`

## Authentication

### Application Passwords (Basic Auth)

Authenticate with a WordPress username and application password over HTTPS.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Site URL:** `siteUrl` · required · Base URL of your WordPress site (for example https://example.com).

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.wordpress.org/rest-api/using-the-rest-api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderby` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
