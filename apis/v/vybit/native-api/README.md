# Vybit: Native API Reference

A consolidated summary of Vybit's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developer.vybit.net/api-reference/
- **OpenAPI specification:** https://developer.vybit.net/api-reference/developer-api.yaml
- **API base URL:** `https://api.vybit.net/v1`

## Authentication

### API Key

Developer API key authentication using the X-API-Key request header.

### Credentials

- **API Key:** `apiKey` · required · API key from the Vybit developer dashboard. MindCloud sends it as the X-API-Key header on every Developer API request.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://developer.vybit.net/api-reference)

### OAuth2

OAuth 2.0 Authorization Code with optional PKCE for accessing Vybit user accounts.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.vybit.net to approve access.
2. Exchange the returned authorization code with a POST request to https://app.vybit.net/service/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


PKCE is enabled.

[Official authentication documentation](https://developer.vybit.net/oauth-reference)

## Pagination

Use `limit` in the query string to set the page size (default 30; accepted range 0–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Reminder](actions/create-reminder.md) | `POST /vybit/{{key}}/reminders` | [docs](https://developer.vybit.net/api-reference/) |
| [Create Vybit](actions/create-vybit.md) | `POST /vybit` | [docs](https://developer.vybit.net/api-reference/) |
| [Delete Reminder](actions/delete-reminder.md) | `DELETE /vybit/{{key}}/reminders/{{reminderId}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Delete Vybit](actions/delete-vybit.md) | `DELETE /vybit/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Get API Status](actions/get-api-status.md) | `GET /status` | [docs](https://developer.vybit.net/api-reference) |
| [Get Log Entry](actions/get-log-entry.md) | `GET /log/{{logKey}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Get Peep](actions/get-peep.md) | `GET /peep/{{key}}` | [docs](https://developer.vybit.net/api-reference) |
| [Get Public Vybit by Subscription Key](actions/get-public-vybit-by-subscription-key.md) | `GET /subscription/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Get Sound Details](actions/get-sound-details.md) | `GET /sound/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Get Subscription Following](actions/get-subscription-following.md) | `GET /subscription/following/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Get Usage Metrics](actions/get-usage-metrics.md) | `GET /meter` | [docs](https://developer.vybit.net/api-reference) |
| [Get User Profile](actions/get-user-profile.md) | `GET /profile` | [docs](https://developer.vybit.net/api-reference/) |
| [Get Vybit](actions/get-vybit.md) | `GET /vybit/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Invite User to Vybit](actions/invite-user-to-vybit.md) | `POST /peep/{{key}}` | [docs](https://developer.vybit.net/api-reference) |
| [List All Logs](actions/list-all-logs.md) | `GET /logs` | [docs](https://developer.vybit.net/api-reference/) |
| [List All Peeps](actions/list-all-peeps.md) | `GET /peeps` | [docs](https://developer.vybit.net/api-reference) |
| [List Logs for Owned Vybit](actions/list-logs-for-owned-vybit.md) | `GET /logs/vybit/{{vybKey}}` | [docs](https://developer.vybit.net/api-reference) |
| [List Logs for Subscription Following](actions/list-logs-for-subscription-following.md) | `GET /logs/subscription/following/{{followingKey}}` | [docs](https://developer.vybit.net/api-reference) |
| [List Peeps for Vybit](actions/list-peeps-for-vybit.md) | `GET /peeps/{{vybitKey}}` | [docs](https://developer.vybit.net/api-reference) |
| [List Public Vybits](actions/list-public-vybits.md) | `GET /subscriptions/public` | [docs](https://developer.vybit.net/api-reference/) |
| [List Reminders](actions/list-reminders.md) | `GET /vybit/{{key}}/reminders` | [docs](https://developer.vybit.net/api-reference/) |
| [List Vybit Subscriptions](actions/list-vybit-subscriptions.md) | `GET /subscriptions/following` | [docs](https://developer.vybit.net/api-reference/) |
| [List Vybits](actions/list-vybits.md) | `GET /vybits` | [docs](https://developer.vybit.net/api-reference/) |
| [List Vybits (Legacy OAuth)](actions/list-vybits-legacy-oauth.md) | `GET /rest/vybit_list` | [docs](https://developer.vybit.net/oauth-reference) |
| [Play Sound](actions/play-sound.md) | `GET /sound/{{key}}/play` | [docs](https://developer.vybit.net/api-reference) |
| [Remove Peep](actions/remove-peep.md) | `DELETE /peep/{{key}}` | [docs](https://developer.vybit.net/api-reference) |
| [Search Sounds](actions/search-sounds.md) | `GET /sounds` | [docs](https://developer.vybit.net/api-reference/) |
| [Send Notification to Group](actions/send-notification-to-group.md) | `POST /subscription/following/{{key}}/send-to-group` | [docs](https://developer.vybit.net/api-reference/) |
| [Send Notification to Owner](actions/send-notification-to-owner.md) | `POST /subscription/following/{{key}}/send-to-owner` | [docs](https://developer.vybit.net/api-reference/) |
| [Subscribe to Vybit](actions/subscribe-to-vybit.md) | `POST /subscription/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Trigger Vybit Notification](actions/trigger-vybit-notification.md) | `POST /vybit/{{key}}/trigger` | [docs](https://developer.vybit.net/api-reference/) |
| [Trigger Vybit Notification (Legacy OAuth)](actions/trigger-vybit-notification-legacy-oauth.md) | `POST /fire/{{triggerKey}}` | [docs](https://developer.vybit.net/oauth-reference) |
| [Unsubscribe from Vybit](actions/unsubscribe-from-vybit.md) | `DELETE /subscription/following/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Update Reminder](actions/update-reminder.md) | `PATCH /vybit/{{key}}/reminders/{{reminderId}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Update Subscription Following](actions/update-subscription-following.md) | `PATCH /subscription/following/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Update Vybit](actions/update-vybit.md) | `PATCH /vybit/{{key}}` | [docs](https://developer.vybit.net/api-reference/) |
| [Validate OAuth Token](actions/validate-oauth-token.md) | `GET /service/test` | [docs](https://developer.vybit.net/oauth-reference) |
