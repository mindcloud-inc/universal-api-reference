# Quiltt: Native API Reference

A consolidated summary of Quiltt's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.quiltt.dev/api-reference
- **API base URL:** `https://api.quiltt.io`

## Authentication

### API Key

Use your Quiltt API secret as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.quiltt.dev/authentication)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Session Token](actions/check-session-token.md) | `GET https://auth.quiltt.io/v1/users/session` | [docs](https://www.quiltt.dev/authentication/managing-session-tokens) |
| [Create Profile](actions/create-profile.md) | `POST /v1/profiles` | [docs](https://www.quiltt.dev/api/profiles) |
| [Create Straddle Processor Token](actions/create-straddle-processor-token.md) | `POST /v1/accounts/:accountId/processor_tokens` | [docs](https://www.quiltt.dev/integrations/payments/straddle) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /v1/webhooks/subscriptions` | [docs](https://www.quiltt.dev/webhooks/setup) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /v1/profiles/:profileId` | [docs](https://www.quiltt.dev/api/profiles) |
| [Get Profile](actions/get-profile.md) | `GET /v1/profiles/:profileId` | [docs](https://www.quiltt.dev/api/profiles) |
| [Issue Session Token](actions/issue-session-token.md) | `POST https://auth.quiltt.io/v1/users/sessions` | [docs](https://www.quiltt.dev/authentication/issuing-session-tokens) |
| [Issue Session Token For New Profile](actions/issue-session-token-for-new-profile.md) | `POST https://auth.quiltt.io/v1/users/sessions` | [docs](https://www.quiltt.dev/authentication/issuing-session-tokens) |
| [List Profiles](actions/list-profiles.md) | `GET /v1/profiles` | [docs](https://www.quiltt.dev/api/profiles) |
| [Revoke Session Token](actions/revoke-session-token.md) | `DELETE https://auth.quiltt.io/v1/users/session` | [docs](https://www.quiltt.dev/authentication/managing-session-tokens) |
| [Update Profile](actions/update-profile.md) | `PATCH /v1/profiles/:profileId` | [docs](https://www.quiltt.dev/api/profiles) |
