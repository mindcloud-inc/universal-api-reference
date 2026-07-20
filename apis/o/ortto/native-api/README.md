# Ortto: Native API Reference

A consolidated summary of Ortto's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.ortto.com/c-49-api-reference
- **API base URL:** `{apiBaseUrl}/v1`

## Authentication

### API Key

Use an Ortto custom private API key in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required
- **API Base URL:** `apiBaseUrl` · required · Region-specific Ortto API host for this workspace. Use https://api.ap3api.com, https://api.eu.ap3api.com, or https://api.au.ap3api.com with no trailing slash.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://help.ortto.com/a-107-configuring-a-custom-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size (default 50; accepted range 1–500). Use `offset` in the request body as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort_by_field_id` in the request body. Set the direction separately with `sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Accounts](actions/archive-accounts.md) | `PUT /accounts/archive` | [docs](https://help.ortto.com/a-279-archive-restore-and-delete-organizations-archive-restore-delete) |
| [Archive Custom Activity](actions/archive-custom-activity.md) | `DELETE /definitions/activity/delete` | [docs](https://help.ortto.com/a-275-delete-a-custom-activity-delete) |
| [Archive People](actions/archive-people.md) | `PUT /person/archive` | [docs](https://help.ortto.com/a-260-archive-restore-and-delete-people-archive-restore-delete) |
| [Create Account Custom Field](actions/create-account-custom-field.md) | `POST /accounts/custom-field/create` | [docs](https://help.ortto.com/a-265-create-a-custom-field-create) |
| [Create Custom Activity Definition](actions/create-custom-activity-definition.md) | `POST /definitions/activity/create` | [docs](https://help.ortto.com/a-273-create-a-custom-activity-definition-create) |
| [Create Custom Activity Event](actions/create-custom-activity-event.md) | `POST /activities/create` | [docs](https://help.ortto.com/a-271-create-a-custom-activity-event-create) |
| [Create Person Custom Field](actions/create-person-custom-field.md) | `POST /person/custom-field/create` | [docs](https://help.ortto.com/a-265-create-a-custom-field-create) |
| [Delete Accounts](actions/delete-accounts.md) | `DELETE /accounts/delete` | [docs](https://help.ortto.com/a-279-archive-restore-and-delete-organizations-archive-restore-delete) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /instances/custom-field/delete` | [docs](https://help.ortto.com/a-908-delete-custom-field) |
| [Delete People](actions/delete-people.md) | `DELETE /person/delete` | [docs](https://help.ortto.com/a-260-archive-restore-and-delete-people-archive-restore-delete) |
| [Export Campaign Data](actions/export-campaign-data.md) | `POST /campaign/get-all` | [docs](https://help.ortto.com/a-887-using-the-api-to-export-campaign-data) |
| [Get Accounts](actions/get-accounts.md) | `POST /accounts/get` | [docs](https://help.ortto.com/a-277-retrieve-one-or-more-organizations-get) |
| [Get Email Suppression List](actions/get-email-suppression-list.md) | `POST /suppression-list/email/get` | [docs](https://help.ortto.com/a-836-managing-the-email-suppression-list-via-api) |
| [Get People](actions/get-people.md) | `POST /person/get` | [docs](https://help.ortto.com/a-258-retrieve-one-or-more-people-get) |
| [Get People Subscription Statuses](actions/get-people-subscription-statuses.md) | `POST /person/subscriptions` | [docs](https://help.ortto.com/a-259-retrieve-peoples-subscription-statuses-subscriptions) |
| [List Account Custom Fields](actions/list-account-custom-fields.md) | `POST /accounts/custom-field/get` | [docs](https://help.ortto.com/a-266-retrieve-a-list-of-custom-fields-get) |
| [List Audiences](actions/list-audiences.md) | `POST /audiences/get` | [docs](https://help.ortto.com/a-268-retrieve-a-list-of-audiences-get) |
| [List Person Custom Fields](actions/list-person-custom-fields.md) | `POST /person/custom-field/get` | [docs](https://help.ortto.com/a-266-retrieve-a-list-of-custom-fields-get) |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | `POST /campaign/calendar` | [docs](https://help.ortto.com/a-695-retrieve-a-list-of-sent-campaigns-calendar) |
| [List Tags](actions/list-tags.md) | `POST /tags/get` | [docs](https://help.ortto.com/a-263-retrieve-a-list-of-tags-get) |
| [Modify Custom Activity Definition](actions/modify-custom-activity-definition.md) | `PUT /definitions/activity/modify` | [docs](https://help.ortto.com/a-274-modify-a-custom-activity-definition-modify) |
| [Remove Email Suppression List Entries](actions/remove-email-suppression-list-entries.md) | `PUT /suppression-list/email/remove` | [docs](https://help.ortto.com/a-836-managing-the-email-suppression-list-via-api) |
| [Restore Accounts](actions/restore-accounts.md) | `PUT /accounts/restore` | [docs](https://help.ortto.com/a-279-archive-restore-and-delete-organizations-archive-restore-delete) |
| [Restore People](actions/restore-people.md) | `PUT /person/restore` | [docs](https://help.ortto.com/a-260-archive-restore-and-delete-people-archive-restore-delete) |
| [Subscribe Audience Members](actions/subscribe-audience-members.md) | `PUT /audience/subscribe` | [docs](https://help.ortto.com/a-269-subscribe-or-unsubscribe-people-to-from-an-audience-subscribe) |
| [Unsubscribe Audience Members](actions/unsubscribe-audience-members.md) | `PUT /audience/subscribe` | [docs](https://help.ortto.com/a-269-subscribe-or-unsubscribe-people-to-from-an-audience-subscribe) |
| [Update Account Custom Field](actions/update-account-custom-field.md) | `PUT /organizations/custom-field/update` | [docs](https://help.ortto.com/a-752-updating-custom-fields-via-the-api) |
| [Update Person Custom Field](actions/update-person-custom-field.md) | `PUT /person/custom-field/update` | [docs](https://help.ortto.com/a-752-updating-custom-fields-via-the-api) |
| [Upsert Accounts](actions/upsert-accounts.md) | `POST /accounts/merge` | [docs](https://help.ortto.com/a-278-create-or-update-one-or-more-organizations-merge) |
| [Upsert People](actions/upsert-people.md) | `POST /person/merge` | [docs](https://help.ortto.com/a-257-create-or-update-one-or-more-people-merge) |
