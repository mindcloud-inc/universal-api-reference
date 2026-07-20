# Pushover: Native API Reference

A consolidated summary of Pushover's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://pushover.net/api
- **API base URL:** `https://api.pushover.net/1`

## Authentication

### API Token

Authenticate with a Pushover application API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pushover.net/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User to Group](actions/add-user-to-group.md) | `POST /groups/:group/add_user.json` | [docs](https://pushover.net/api/groups#add_user) |
| [Cancel Emergency Receipt](actions/cancel-emergency-receipt.md) | `POST /receipts/:receipt/cancel.json` | [docs](https://pushover.net/api/receipts#cancel) |
| [Cancel Emergency Receipts by Tag](actions/cancel-emergency-receipts-by-tag.md) | `POST /receipts/cancel_by_tag/:tag.json` | [docs](https://pushover.net/api/receipts#cancel_by_tag) |
| [Disable Group User](actions/disable-group-user.md) | `POST /groups/:group/disable_user.json` | [docs](https://pushover.net/api/groups#disable_user) |
| [Enable Group User](actions/enable-group-user.md) | `POST /groups/:group/enable_user.json` | [docs](https://pushover.net/api/groups#enable_user) |
| [Get App Limits](actions/get-app-limits.md) | `GET /apps/limits.json` | [docs](https://pushover.net/api#limits) |
| [Get Group](actions/get-group.md) | `GET /groups/:group.json` | [docs](https://pushover.net/api/groups#show) |
| [Get Receipt Status](actions/get-receipt-status.md) | `GET /receipts/:receipt.json` | [docs](https://pushover.net/api/receipts) |
| [List Groups](actions/list-groups.md) | `GET /groups.json` | [docs](https://pushover.net/api/groups#list) |
| [List Sounds](actions/list-sounds.md) | `GET /sounds.json` | [docs](https://pushover.net/api#sounds) |
| [Migrate Subscription User Key](actions/migrate-subscription-user-key.md) | `POST /subscriptions/migrate.json` | [docs](https://pushover.net/api/subscriptions#migration) |
| [Remove User from Group](actions/remove-user-from-group.md) | `POST /groups/:group/remove_user.json` | [docs](https://pushover.net/api/groups#remove_user) |
| [Rename Group](actions/rename-group.md) | `POST /groups/:group/rename.json` | [docs](https://pushover.net/api/groups#rename) |
| [Send Message](actions/send-message.md) | `POST /messages.json` | [docs](https://pushover.net/api#messages) |
| [Update Glance](actions/update-glance.md) | `POST /glances.json` | [docs](https://pushover.net/api/glances#update) |
| [Validate User or Group](actions/validate-user-or-group.md) | `POST /users/validate.json` | [docs](https://pushover.net/api#validate) |
