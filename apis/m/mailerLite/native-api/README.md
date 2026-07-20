# MailerLite: Native API Reference

A consolidated summary of MailerLite's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://developers.mailerlite.com/docs/
- **API base URL:** `https://connect.mailerlite.com/api`

## Authentication

### API Key

MailerLite API token used as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-mailerlite-apikey: <apiKey>
```

[Official authentication documentation](https://developers.mailerlite.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `meta.next_cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Subscriber to Group](actions/assign-subscriber-to-group.md) | `POST /subscribers/:subscriber_id/groups/:group_id` | [docs](https://developers.mailerlite.com/docs/groups#assign-subscriber-to-a-group) |
| [Cancel Ready Campaign](actions/cancel-ready-campaign.md) | `POST /campaigns/:campaignId/cancel` | [docs](https://developers.mailerlite.com/docs/campaigns#cancel-a-ready-campaign) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://developers.mailerlite.com/docs/campaigns#create-a-campaign) |
| [Create Draft Automation](actions/create-draft-automation.md) | `POST /automations` | [docs](https://developers.mailerlite.com/docs/automations#create-draft-automation) |
| [Create Field](actions/create-field.md) | `POST /fields` | [docs](https://developers.mailerlite.com/docs/fields#create-a-field) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://developers.mailerlite.com/docs/groups#create-a-group) |
| [Create or Upsert Subscriber](actions/create-or-upsert-subscriber.md) | `POST /subscribers` | [docs](https://developers.mailerlite.com/docs/subscribers#create-upsert-subscriber) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.mailerlite.com/docs/webhooks#create-a-webhook) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /subscribers/:id` | [docs](https://developers.mailerlite.com/docs/subscribers#delete-a-subscriber) |
| [Forget Subscriber](actions/forget-subscriber.md) | `POST /subscribers/:id/forget` | [docs](https://developers.mailerlite.com/docs/subscribers#forget-a-subscriber) |
| [Get Automation](actions/get-automation.md) | `GET /automations/:automationId` | [docs](https://developers.mailerlite.com/docs/automations#get-an-automation) |
| [Get Automation Subscriber Activity](actions/get-automation-subscriber-activity.md) | `GET /automations/:automationId/activity` | [docs](https://developers.mailerlite.com/docs/automations#get-the-subscriber-activity-for-an-automation) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://developers.mailerlite.com/docs/campaigns#get-a-campaign) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:idOrEmail` | [docs](https://developers.mailerlite.com/docs/subscribers#fetch-a-subscriber) |
| [Get Subscriber Activity](actions/get-subscriber-activity.md) | `GET /subscribers/:id/activity-log` | [docs](https://developers.mailerlite.com/docs/subscribers#fetch-subscriber-activity) |
| [Import Bulk Subscribers to Group](actions/import-bulk-subscribers-to-group.md) | `POST /groups/:group_id/import-subscribers` | [docs](https://developers.mailerlite.com/docs/groups#import-bulk-subscribers-to-group) |
| [List Automations](actions/list-automations.md) | `GET /automations` | [docs](https://developers.mailerlite.com/docs/automations#list-all-automations) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developers.mailerlite.com/docs/campaigns#campaign-list) |
| [List Fields](actions/list-fields.md) | `GET /fields` | [docs](https://developers.mailerlite.com/docs/fields#list-all-fields) |
| [List Group Subscribers](actions/list-group-subscribers.md) | `GET /groups/:group_id/subscribers` | [docs](https://developers.mailerlite.com/docs/groups#get-subscribers-belonging-to-a-group) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://developers.mailerlite.com/docs/groups#list-all-groups) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://developers.mailerlite.com/docs/segments#list-all-segments) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers` | [docs](https://developers.mailerlite.com/docs/subscribers#list-all-subscribers) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.mailerlite.com/docs/webhooks#list-all-webhooks) |
| [Schedule Campaign](actions/schedule-campaign.md) | `POST /campaigns/:campaignId/schedule` | [docs](https://developers.mailerlite.com/docs/campaigns#schedule-a-campaign) |
| [Unassign Subscriber from Group](actions/unassign-subscriber-from-group.md) | `DELETE /subscribers/:subscriber_id/groups/:group_id` | [docs](https://developers.mailerlite.com/docs/groups#unassign-subscriber-from-a-group) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaigns/:campaignId` | [docs](https://developers.mailerlite.com/docs/campaigns#update-campaign) |
| [Update Group](actions/update-group.md) | `PUT /groups/:group_id` | [docs](https://developers.mailerlite.com/docs/groups#update-a-group) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /subscribers/:id` | [docs](https://developers.mailerlite.com/docs/subscribers#update-a-subscriber) |
