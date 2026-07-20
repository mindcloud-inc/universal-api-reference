# <img src="https://images.mindcloud.co/apps/icons/send-x_1774552618266.png" alt="SendX logo" width="28" height="28"> SendX: Universal API

Manage SendX contacts, lists, campaigns, and email templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendX/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sendx.io/
- **Vendor API docs:** https://docs.sendx.io/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [Get Campaign Report](actions/get-campaign-report.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Identify Bulk Contacts](actions/identify-bulk-contacts.md) | POST |  |
| [Identify Contact](actions/identify-contact.md) | POST |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST |  |
| [Get Custom Field](actions/get-custom-field.md) | GET |  |
| [List Custom Fields](actions/list-custom-fields.md) | GET |  |
| [Update Custom Field](actions/update-custom-field.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Template](actions/create-email-template.md) | POST |  |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Get List](actions/get-list.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |
| [Update List](actions/update-list.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

