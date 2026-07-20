# Adafruit IO: Native API Reference

A consolidated summary of Adafruit IO's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://io.adafruit.com/api/docs/
- **API base URL:** `https://io.adafruit.com/api/v2`

## Authentication

### Adafruit IO Key

Use the Adafruit IO Key with the account username. The key is copied from the golden key icon / View Adafruit IO Key UI.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Adafruit IO username used in API paths like /api/v2/{username}/...

Send these headers with each API request:

```http
X-AIO-Key: <apiKey>
```

[Official authentication documentation](https://io.adafruit.com/api/docs/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 1000; maximum 1000). Use `before` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Feed to Group](actions/add-feed-to-group.md) | `POST /{{credentials.username}}/groups/:group_key/add` | [docs](https://io.adafruit.com/api/docs/#add-feed-to-group) |
| [Chart Feed Data](actions/chart-feed-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/chart` | [docs](https://io.adafruit.com/api/docs/#chart-feed-data) |
| [Create Action](actions/create-action.md) | `POST /{{credentials.username}}/actions` | [docs](https://io.adafruit.com/api/docs/#create-action) |
| [Create Data](actions/create-data.md) | `POST /{{credentials.username}}/feeds/:feed_key/data` | [docs](https://io.adafruit.com/api/docs/#create-data) |
| [Create Feed](actions/create-feed.md) | `POST /{{credentials.username}}/feeds` | [docs](https://io.adafruit.com/api/docs/#create-feed) |
| [Create Feed in a Group](actions/create-feed-in-a-group.md) | `POST /{{credentials.username}}/groups/:group_key/feeds` | [docs](https://io.adafruit.com/api/docs/#create-feed-in-a-group) |
| [Create Group](actions/create-group.md) | `POST /{{credentials.username}}/groups` | [docs](https://io.adafruit.com/api/docs/#create-group) |
| [Create Multiple Data Records](actions/create-multiple-data-records.md) | `POST /{{credentials.username}}/feeds/:feed_key/data/batch` | [docs](https://io.adafruit.com/api/docs/#create-multiple-data-records) |
| [Create Token](actions/create-token.md) | `POST /{{credentials.username}}/tokens` | [docs](https://io.adafruit.com/api/docs/#create-token) |
| [Delete Action](actions/delete-action.md) | `DELETE /{{credentials.username}}/actions/:id` | [docs](https://io.adafruit.com/api/docs/#delete-action) |
| [Delete Data Point](actions/delete-data-point.md) | `DELETE /{{credentials.username}}/feeds/:feed_key/data/:id` | [docs](https://io.adafruit.com/api/docs/#delete-data-point) |
| [Delete Feed](actions/delete-feed.md) | `DELETE /{{credentials.username}}/feeds/:feed_key` | [docs](https://io.adafruit.com/api/docs/#delete-feed) |
| [Delete Group](actions/delete-group.md) | `DELETE /{{credentials.username}}/groups/:group_key` | [docs](https://io.adafruit.com/api/docs/#delete-group) |
| [Delete Token](actions/delete-token.md) | `DELETE /{{credentials.username}}/tokens/:id` | [docs](https://io.adafruit.com/api/docs/#delete-token) |
| [Get Action](actions/get-action.md) | `GET /{{credentials.username}}/actions/:id` | [docs](https://io.adafruit.com/api/docs/#return-action) |
| [Get Data Point](actions/get-data-point.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/:id` | [docs](https://io.adafruit.com/api/docs/#get-data-point) |
| [Get Detailed User Info](actions/get-detailed-user-info.md) | `GET /{{credentials.username}}/throttle` | [docs](https://io.adafruit.com/api/docs/#get-detailed-user-info) |
| [Get Feed](actions/get-feed.md) | `GET /{{credentials.username}}/feeds/:feed_key` | [docs](https://io.adafruit.com/api/docs/#get-feed) |
| [Get First Data](actions/get-first-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/first` | [docs](https://io.adafruit.com/api/docs/#get-first-data) |
| [Get Group](actions/get-group.md) | `GET /{{credentials.username}}/groups/:group_key` | [docs](https://io.adafruit.com/api/docs/#get-group) |
| [Get Last Data](actions/get-last-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/last` | [docs](https://io.adafruit.com/api/docs/#get-last-data) |
| [Get Most Recent Data](actions/get-most-recent-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/retain` | [docs](https://io.adafruit.com/api/docs/#get-most-recent-data) |
| [Get Next Data](actions/get-next-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/next` | [docs](https://io.adafruit.com/api/docs/#get-next-data) |
| [Get Previous Data](actions/get-previous-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data/previous` | [docs](https://io.adafruit.com/api/docs/#get-previous-data) |
| [Get Token](actions/get-token.md) | `GET /{{credentials.username}}/tokens/:id` | [docs](https://io.adafruit.com/api/docs/#returns-token) |
| [Get User Info](actions/get-user-info.md) | `GET /user` | [docs](https://io.adafruit.com/api/docs/#get-user-info) |
| [List Actions](actions/list-actions.md) | `GET /{{credentials.username}}/actions` | [docs](https://io.adafruit.com/api/docs/#get-all-actions) |
| [List Feed Data](actions/list-feed-data.md) | `GET /{{credentials.username}}/feeds/:feed_key/data` | [docs](https://io.adafruit.com/api/docs/#get-feed-data) |
| [List Feeds](actions/list-feeds.md) | `GET /{{credentials.username}}/feeds` | [docs](https://io.adafruit.com/api/docs/#all-feeds) |
| [List Group Feeds](actions/list-group-feeds.md) | `GET /{{credentials.username}}/groups/:group_key/feeds` | [docs](https://io.adafruit.com/api/docs/#get-group-feeds) |
| [List Groups](actions/list-groups.md) | `GET /{{credentials.username}}/groups` | [docs](https://io.adafruit.com/api/docs/#get-all-groups) |
| [List Tokens](actions/list-tokens.md) | `GET /{{credentials.username}}/tokens` | [docs](https://io.adafruit.com/api/docs/#get-all-tokens) |
| [Remove Feed from Group](actions/remove-feed-from-group.md) | `POST /{{credentials.username}}/groups/:group_key/remove` | [docs](https://io.adafruit.com/api/docs/#remove-feed-from-group) |
| [Replace Action](actions/replace-action.md) | `PUT /{{credentials.username}}/actions/:id` | [docs](https://io.adafruit.com/api/docs/#replace-action) |
| [Send Arbitrary Data via Webhook](actions/send-arbitrary-data-via-webhook.md) | `POST /webhooks/feed/:token/raw` | [docs](https://io.adafruit.com/api/docs/#send-arbitrary-data-via-webhook) |
| [Send Data via Webhook](actions/send-data-via-webhook.md) | `POST /webhooks/feed/:token` | [docs](https://io.adafruit.com/api/docs/#send-data-via-webhook) |
| [Send Notification via Webhook](actions/send-notification-via-webhook.md) | `POST /webhooks/feed/:token/notify` | [docs](https://io.adafruit.com/api/docs/#send-notification-via-webhook) |
| [Update Data Point](actions/update-data-point.md) | `PUT /{{credentials.username}}/feeds/:feed_key/data/:id` | [docs](https://io.adafruit.com/api/docs/#update-data-point) |
| [Update Feed](actions/update-feed.md) | `PUT /{{credentials.username}}/feeds/:feed_key` | [docs](https://io.adafruit.com/api/docs/#update-feed) |
| [Update Group](actions/update-group.md) | `PUT /{{credentials.username}}/groups/:group_key` | [docs](https://io.adafruit.com/api/docs/#update-group) |
