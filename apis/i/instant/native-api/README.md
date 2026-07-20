# Instant: Native API Reference

A consolidated summary of Instant's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.instantdb.com/docs/http-api
- **API base URL:** `https://api.instantdb.com`

## Authentication

### Admin Token

Use an Instant admin token plus app ID for Admin HTTP API access.

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · Your Instant app ID.

Send these headers with each API request:

```http
App-Id: <appId>
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.instantdb.com/docs/http-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Transact Steps](actions/batch-transact-steps.md) | `POST /admin/transact` | [docs](https://www.instantdb.com/docs/http-api) |
| [Create Custom Magic Code](actions/create-custom-magic-code.md) | `POST /admin/magic_code` | [docs](https://www.instantdb.com/docs/http-api) |
| [Create Refresh Token by Email](actions/create-refresh-token-by-email.md) | `POST /admin/refresh_tokens` | [docs](https://www.instantdb.com/docs/http-api) |
| [Create Refresh Token by Email With Extra Fields](actions/create-refresh-token-by-email-with-extra-fields.md) | `POST /admin/refresh_tokens` | [docs](https://www.instantdb.com/docs/http-api) |
| [Create Refresh Token by User ID](actions/create-refresh-token-by-user-id.md) | `POST /admin/refresh_tokens` | [docs](https://www.instantdb.com/docs/http-api) |
| [Create Refresh Token by User ID With Extra Fields](actions/create-refresh-token-by-user-id-with-extra-fields.md) | `POST /admin/refresh_tokens` | [docs](https://www.instantdb.com/docs/http-api) |
| [Delete File](actions/delete-file.md) | `DELETE /admin/storage/files` | [docs](https://www.instantdb.com/docs/http-api) |
| [Delete Files](actions/delete-files.md) | `POST /admin/storage/files/delete` | [docs](https://www.instantdb.com/docs/http-api) |
| [Delete User by Email](actions/delete-user-by-email.md) | `DELETE /admin/users` | [docs](https://www.instantdb.com/docs/http-api) |
| [Delete User by ID](actions/delete-user-by-id.md) | `DELETE /admin/users` | [docs](https://www.instantdb.com/docs/http-api) |
| [Delete User by Refresh Token](actions/delete-user-by-refresh-token.md) | `DELETE /admin/users` | [docs](https://www.instantdb.com/docs/http-api) |
| [Get Room Presence](actions/get-room-presence.md) | `GET /admin/rooms/presence` | [docs](https://www.instantdb.com/docs/http-api) |
| [Get User by Email](actions/get-user-by-email.md) | `GET /admin/users` | [docs](https://www.instantdb.com/docs/http-api) |
| [Get User by ID](actions/get-user-by-id.md) | `GET /admin/users` | [docs](https://www.instantdb.com/docs/http-api) |
| [Get User by Refresh Token](actions/get-user-by-refresh-token.md) | `GET /admin/users` | [docs](https://www.instantdb.com/docs/http-api) |
| [List Files](actions/list-files.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [List Users](actions/list-users.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [Query Records](actions/query-records.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [Query Records As Email](actions/query-records-as-email.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [Query Records As Guest](actions/query-records-as-guest.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [Query Records As Refresh Token](actions/query-records-as-refresh-token.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [Query Records With Rule Params](actions/query-records-with-rule-params.md) | `POST /admin/query` | [docs](https://www.instantdb.com/docs/http-api) |
| [Send Magic Code](actions/send-magic-code.md) | `POST /admin/send_magic_code` | [docs](https://www.instantdb.com/docs/http-api) |
| [Sign Out Session by Refresh Token](actions/sign-out-session-by-refresh-token.md) | `POST /admin/sign_out` | [docs](https://www.instantdb.com/docs/http-api) |
| [Sign Out User by Email](actions/sign-out-user-by-email.md) | `POST /admin/sign_out` | [docs](https://www.instantdb.com/docs/http-api) |
| [Sign Out User by ID](actions/sign-out-user-by-id.md) | `POST /admin/sign_out` | [docs](https://www.instantdb.com/docs/http-api) |
| [Upload File](actions/upload-file.md) | `PUT /admin/storage/upload` | [docs](https://www.instantdb.com/docs/http-api) |
| [Verify Magic Code](actions/verify-magic-code.md) | `POST /admin/verify_magic_code` | [docs](https://www.instantdb.com/docs/http-api) |
| [Verify Magic Code With Extra Fields](actions/verify-magic-code-with-extra-fields.md) | `POST /admin/verify_magic_code` | [docs](https://www.instantdb.com/docs/http-api) |
| [Verify Refresh Token](actions/verify-refresh-token.md) | `POST /runtime/auth/verify_refresh_token` | [docs](https://www.instantdb.com/docs/http-api) |
