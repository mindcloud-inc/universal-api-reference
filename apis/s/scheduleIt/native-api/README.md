# Schedule It: Native API Reference

A consolidated summary of Schedule It's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks
- **API base URL:** `https://www.scheduleit.com/api`

## Authentication

### HTTP Basic

Use your Schedule It account login and password.

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

[Official authentication documentation](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_workspace` | query | `string` | no | Use a workspace ID to query records outside the main workspace. |

Responses from this API use JSON.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `lt`, `ne`.

## Retry behavior

Retry responses with status codes `429`. Wait 60000 ms before the first retry. Stop after 1 attempts.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Create Resource](actions/create-resource.md) | `POST /resources` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Delete Resource](actions/delete-resource.md) | `DELETE /resources/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Get Label](actions/get-label.md) | `GET /labels/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Update Event](actions/update-event.md) | `POST /events/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Update Group](actions/update-group.md) | `POST /groups/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
| [Update Resource](actions/update-resource.md) | `POST /resources/:id` | [docs](https://www.scheduleit.com/faq/10640/is-there-a-rest-api-or-webhooks) |
