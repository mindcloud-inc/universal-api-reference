# <img src="https://images.mindcloud.co/apps/icons/icon_1773685460719.png" alt="Ortto logo" width="28" height="28"> Ortto: Universal API

Manage customer data, audiences, and marketing activity in Ortto

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ortto/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ortto.com
- **Vendor API docs:** https://help.ortto.com/c-49-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Export Campaign Data](actions/export-campaign-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/export-campaign-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Export Campaign Data](actions/export-campaign-data.md) | GET |  |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | GET |  |

### Custom Activity

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Activity Event](actions/create-custom-activity-event.md) | POST |  |

### Custom Activity Definition

| Action | Method | Description |
| --- | --- | --- |
| [Archive Custom Activity](actions/archive-custom-activity.md) | DELETE |  |
| [Create Custom Activity Definition](actions/create-custom-activity-definition.md) | POST |  |
| [Modify Custom Activity Definition](actions/modify-custom-activity-definition.md) | PUT |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Custom Field](actions/create-account-custom-field.md) | POST |  |
| [Create Person Custom Field](actions/create-person-custom-field.md) | POST |  |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE |  |
| [List Account Custom Fields](actions/list-account-custom-fields.md) | GET |  |
| [List Person Custom Fields](actions/list-person-custom-fields.md) | GET |  |
| [Update Account Custom Field](actions/update-account-custom-field.md) | PUT |  |
| [Update Person Custom Field](actions/update-person-custom-field.md) | PUT |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Archive Accounts](actions/archive-accounts.md) | PUT |  |
| [Archive People](actions/archive-people.md) | PUT |  |
| [Delete Accounts](actions/delete-accounts.md) | DELETE |  |
| [Delete People](actions/delete-people.md) | DELETE |  |
| [Get Accounts](actions/get-accounts.md) | GET |  |
| [Get Email Suppression List](actions/get-email-suppression-list.md) | GET |  |
| [Get People](actions/get-people.md) | GET |  |
| [Get People Subscription Statuses](actions/get-people-subscription-statuses.md) | GET |  |
| [List Audiences](actions/list-audiences.md) | GET |  |
| [Remove Email Suppression List Entries](actions/remove-email-suppression-list-entries.md) | PUT |  |
| [Restore Accounts](actions/restore-accounts.md) | PUT |  |
| [Restore People](actions/restore-people.md) | PUT |  |
| [Subscribe Audience Members](actions/subscribe-audience-members.md) | PUT |  |
| [Unsubscribe Audience Members](actions/unsubscribe-audience-members.md) | PUT |  |
| [Upsert Accounts](actions/upsert-accounts.md) | POST |  |
| [Upsert People](actions/upsert-people.md) | POST |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

