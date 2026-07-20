# AnnounceKit: Native API Reference

A consolidated summary of AnnounceKit's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://announcekit.app/docs/graphql-api
- **API base URL:** `https://announcekit.app`

## Authentication

### Basic Authentication

Authenticate AnnounceKit GraphQL API requests with HTTP Basic Authentication. Enter the raw AnnounceKit dashboard username/email and password in the connection fields; MindCloud will build the Authorization header.

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

[Official authentication documentation](https://announcekit.app/docs/graphql-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Draft Post](actions/create-draft-post.md) | `POST /gq/v2` | [docs](https://announcekit.app/docs/graphql-api) |
| [Get Active Project](actions/get-active-project.md) | `POST /gq/v2` | [docs](https://announcekit.app/docs/graphql-api) |
| [List Labels](actions/list-labels.md) | `POST /gq/v2` | [docs](https://announcekit.app/docs/graphql-api) |
| [Publish Post](actions/publish-post.md) | `POST /gq/v2` | [docs](https://announcekit.app/docs/graphql-api) |
