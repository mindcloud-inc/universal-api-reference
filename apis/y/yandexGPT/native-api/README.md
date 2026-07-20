# YandexGPT: Native API Reference

A consolidated summary of YandexGPT's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://aistudio.yandex.ru/docs/en/ai-studio/
- **API base URL:** `https://ai.api.cloud.yandex.net`

## Authentication

### OAuth2

Authenticate with a Yandex account, then exchange the OAuth token for a short-lived Yandex Cloud IAM token for API calls.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://oauth.yandex.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.yandex.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `login:avatar login:birthday login:email login:info login:default_phone`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth.yandex.com/token.

[Official authentication documentation](https://yandex.com/dev/id/doc/en/how-to)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | `GET /v1/models/:model_id` | [docs](https://yandex.cloud/en/docs/ai-studio/models/getModel) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://yandex.cloud/en/docs/ai-studio/models/listModels) |
