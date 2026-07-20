# Supernotes: Native API Reference

A consolidated summary of Supernotes's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.supernotes.app/api-reference/introduction
- **OpenAPI specification:** https://api.supernotes.app/openapi.json
- **API base URL:** `https://api.supernotes.app/v1`

## Authentication

### API Key

Connect with a Supernotes API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.supernotes.app/api-reference/user/check-auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Auth](actions/check-auth.md) | `GET /user/token` | [docs](https://developer.supernotes.app/api-reference/user/check-auth) |
| [Check If Fresh Access Token](actions/check-if-fresh-access-token.md) | `GET /user/token/fresh` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Find Card By Share Code](actions/find-card-by-share-code.md) | `GET /sharing/code/:code` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get All Templates](actions/get-all-templates.md) | `GET /templates` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Announcements](actions/get-announcements.md) | `GET /announcements/` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get API Version Meta](actions/get-api-version-meta.md) | `GET /` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Card](actions/get-card.md) | `GET /cards/:card_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Collection](actions/get-collection.md) | `GET /collections/:collection_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Collections](actions/get-collections.md) | `GET /collections` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Comments](actions/get-comments.md) | `GET /comments/:card_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /profiles` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Deleted Cards](actions/get-deleted-cards.md) | `GET /cards/get/deleted` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Deleted Collections](actions/get-deleted-collections.md) | `GET /collections/deleted` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Email](actions/get-email.md) | `GET /user/emails/:email_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Friends](actions/get-friends.md) | `GET /friends` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Incoming Requests](actions/get-incoming-requests.md) | `GET /friends/incoming` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Known Owner Profiles](actions/get-known-owner-profiles.md) | `GET /profiles/known` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Members](actions/get-members.md) | `GET /members/:card_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Other User Profile](actions/get-other-user-profile.md) | `GET /profiles/:user_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Outgoing Requests](actions/get-outgoing-requests.md) | `GET /friends/outgoing` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Pins](actions/get-pins.md) | `GET /user/pins` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Selected Cards](actions/get-selected-cards.md) | `POST /cards/get/select` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Share Codes For Card](actions/get-share-codes-for-card.md) | `GET /sharing/:card_id` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Synth Credits](actions/get-synth-credits.md) | `GET /synth/credits` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get User API Keys](actions/get-user-api-keys.md) | `GET /keys` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get User Email Addresses](actions/get-user-email-addresses.md) | `GET /user/emails` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get User Sending Email](actions/get-user-sending-email.md) | `GET /keys/email` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get User Webhooks](actions/get-user-webhooks.md) | `GET /webhooks` | [docs](https://developer.supernotes.app/api-reference/introduction) |
| [Get Users Tags](actions/get-users-tags.md) | `GET /tags` | [docs](https://developer.supernotes.app/api-reference/introduction) |
