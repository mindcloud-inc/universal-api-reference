# Cloud BOT: Native API Reference

A consolidated summary of Cloud BOT's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.c-bot.pro/en/api_reference/
- **API base URL:** `https://api.c-bot.pro`

## Authentication

### OAuth 2.0

Connect Cloud BOT using the official OAuth 2.0 authorization code flow for user-authorized access to Cloud BOT APIs.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://console.c-bot.pro/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://console.c-bot.pro/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `refer`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://console.c-bot.pro/oauth/token.

[Official authentication documentation](https://docs.c-bot.pro/wp-content/uploads/2023/12/oauth2-v1-en.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bot Subscription](actions/create-bot-subscription.md) | `POST /:public_id/bots/:bot_id/subscriptions` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/post-public_id-bots-bot_id-subscriptions) |
| [Delete Bot Subscription](actions/delete-bot-subscription.md) | `DELETE /:public_id/bots/:bot_id/subscriptions/:subscribe_id` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/delete-public_id-bots-bot_id-subscriptions-subscribe_id) |
| [Export Bot Definition](actions/export-bot-definition.md) | `GET /:public_id/bots/:bot_id/definition` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots-bot_id-definition) |
| [Get Bot Details](actions/get-bot-details.md) | `GET /:public_id/bots/:bot_id` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots-bot_id) |
| [Get Job](actions/get-job.md) | `GET /:public_id/jobs/:job_id` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-jobs-job_id) |
| [Issue WS Token](actions/issue-ws-token.md) | `POST /:public_id/ws_tokens` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/post-public_id-ws_tokens) |
| [List Bot Jobs](actions/list-bot-jobs.md) | `GET /:public_id/bots/:bot_id/jobs` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots-bot_id-jobs) |
| [List Bot Subscriptions](actions/list-bot-subscriptions.md) | `GET /:public_id/bots/:bot_id/subscriptions` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots-bot_id-subscriptions) |
| [List Bots](actions/list-bots.md) | `GET /:public_id/bots` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots) |
| [List Contracts](actions/list-contracts.md) | `GET /services/contracts` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-services-contracts) |
| [Run Bot](actions/run-bot.md) | `POST /:public_id/bots/:bot_id/jobs` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/post-public_id-bots-bot_id-jobs) |
| [Suspend Job](actions/suspend-job.md) | `DELETE /:public_id/jobs/:job_id` | [docs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/delete-public_id-jobs-job_id) |
