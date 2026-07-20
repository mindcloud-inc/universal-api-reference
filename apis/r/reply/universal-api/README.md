# Reply: Universal API

Manage Reply campaigns, contacts, sequences, schedules, and outreach emails

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reply/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://reply.io/
- **Vendor API docs:** https://apidocs.reply.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get List of Campaigns](actions/get-list-of-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-list-of-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Get Campaign By Id](actions/get-campaign-by-id.md) | GET |  |
| [Get List of Campaigns](actions/get-list-of-campaigns.md) | GET |  |
| [Pause Campaign](actions/pause-campaign.md) | PUT |  |
| [Start Campaign](actions/start-campaign.md) | PUT |  |
| [Update Campaign Settings](actions/update-campaign-settings.md) | PUT |  |

### Campaign Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Push Contact To Sequence](actions/push-contact-to-sequence.md) | PUT |  |
| [Remove Contact From Sequence](actions/remove-contact-from-sequence.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create New Contact](actions/create-new-contact.md) | POST |  |
| [Delete Contact By Id](actions/delete-contact-by-id.md) | DELETE |  |
| [Get All Contacts](actions/get-all-contacts.md) | GET |  |
| [Get Contact By Email](actions/get-contact-by-email.md) | GET |  |
| [Get Contact By Id](actions/get-contact-by-id.md) | GET |  |
| [Lookup Prospect Id](actions/lookup-prospect-id.md) | GET |  |
| [Update Contact By Email](actions/update-contact-by-email.md) | PUT |  |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Fields](actions/get-custom-fields.md) | GET |  |

### Direct Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Direct Email To Prospect](actions/send-direct-email-to-prospect.md) | POST |  |

### Email Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Accounts](actions/get-email-accounts.md) | GET |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Get All Lists](actions/get-all-lists.md) | GET |  |
| [Get Contacts In List](actions/get-contacts-in-list.md) | GET |  |

### List Membership

| Action | Method | Description |
| --- | --- | --- |
| [Move Contact To List](actions/move-contact-to-list.md) | PUT |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedules](actions/get-schedules.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Templates](actions/get-templates.md) | GET |  |

