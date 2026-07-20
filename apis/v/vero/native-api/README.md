# Vero: Native API Reference

A consolidated summary of Vero's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://help.getvero.com/api-reference/track/overview
- **API base URL:** `https://api.getvero.com`

## Authentication

### Authentication Token

Use a Vero Authentication Token. Vero's Track API expects the token as the auth_token query parameter on requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.getvero.com/api-reference/track/overview)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Alias](actions/alias.md) | `PUT /api/v2/users/reidentify` | [docs](https://help.getvero.com/api-reference/users/alias) |
| [Cancel Campaign](actions/cancel-campaign.md) | `DELETE /api/v4/campaigns/:id/cancel` | [docs](https://help.getvero.com/api-reference/campaigns/cancels-a-campaign) |
| [Create Campaign](actions/create-campaign.md) | `POST /api/v4/campaigns` | [docs](https://help.getvero.com/api-reference/campaigns/create-a-campaign) |
| [Delete User](actions/delete-user.md) | `POST /api/v2/users/delete` | [docs](https://help.getvero.com/api-reference/users/delete) |
| [Edit Tags](actions/edit-tags.md) | `PUT /api/v2/users/tags/edit` | [docs](https://help.getvero.com/api-reference/tags/edit) |
| [Get Trigger](actions/get-trigger.md) | `GET /api/v4/triggers/:id` | [docs](https://help.getvero.com/api-reference/trigger/returns-a-trigger) |
| [Identify](actions/identify.md) | `POST /api/v2/users/track` | [docs](https://help.getvero.com/api-reference/users/identify) |
| [Launch Campaign](actions/launch-campaign.md) | `POST /api/v4/campaigns/:id/launch` | [docs](https://help.getvero.com/api-reference/campaigns/launch-a-campaign) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/v4/campaigns` | [docs](https://help.getvero.com/api-reference/campaigns/returns-campaigns) |
| [List Messages](actions/list-messages.md) | `GET /api/v4/messages` | [docs](https://help.getvero.com/api-reference/messages/returns-messages) |
| [Resubscribe](actions/resubscribe.md) | `POST /api/v2/users/resubscribe` | [docs](https://help.getvero.com/api-reference/users/resubscribe) |
| [Retrieve Campaign](actions/retrieve-campaign.md) | `GET /api/v4/campaigns/:id` | [docs](https://help.getvero.com/api-reference/campaigns/retrieve-a-campaign) |
| [Retrieve Message](actions/retrieve-message.md) | `GET /api/v4/messages/:id` | [docs](https://help.getvero.com/api-reference/messages/retrieve-a-message) |
| [Track Event](actions/track-event.md) | `POST /api/v2/events/track` | [docs](https://help.getvero.com/api-reference/events/track) |
| [Unsubscribe](actions/unsubscribe.md) | `POST /api/v2/users/unsubscribe` | [docs](https://help.getvero.com/api-reference/users/unsubscribe) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /api/v4/campaigns/:id` | [docs](https://help.getvero.com/api-reference/campaigns/update-a-campaign) |
| [Update Message](actions/update-message.md) | `PATCH /api/v4/messages/:id` | [docs](https://help.getvero.com/api-reference/messages/update-an-email-message) |
| [Update Trigger](actions/update-trigger.md) | `PATCH /api/v4/triggers/:id` | [docs](https://help.getvero.com/api-reference/trigger/updates-a-trigger) |
