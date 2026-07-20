# <img src="https://images.mindcloud.co/apps/icons/cloud-contact-ai_1782741470340.png" alt="CloudContactAI logo" width="28" height="28"> CloudContactAI: Universal API

CloudContactAI lets you manage clients, contacts, campaigns, collection settings, and SMS messaging with bearer-token authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudContactAI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudcontactai.com
- **Vendor API docs:** https://developer.cloudcontactai.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Create Client Campaign](actions/create-client-campaign.md) | POST |  |
| [Create Collection Campaign](actions/create-collection-campaign.md) | POST |  |
| [Create Direct Campaign](actions/create-direct-campaign.md) | POST |  |
| [Delete Campaign by ID](actions/delete-campaign-by-id.md) | DELETE |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [List Client Campaigns](actions/list-client-campaigns.md) | GET |  |
| [Requeue Campaign](actions/requeue-campaign.md) | PUT |  |
| [Send Campaign Messages](actions/send-campaign-messages.md) | POST |  |
| [Update Client Campaign](actions/update-client-campaign.md) | PUT |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Delete Client by ID](actions/delete-client-by-id.md) | DELETE |  |
| [Get Client by ID](actions/get-client-by-id.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Patch Client by ID](actions/patch-client-by-id.md) | PUT |  |
| [Update Client by ID](actions/update-client-by-id.md) | PUT |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Batch Create Contacts](actions/batch-create-contacts.md) | POST |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact by ID](actions/delete-contact-by-id.md) | DELETE |  |
| [Get Contact by ID](actions/get-contact-by-id.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Contacts with Email](actions/list-contacts-with-email.md) | GET |  |
| [List Contacts with Phone](actions/list-contacts-with-phone.md) | GET |  |
| [List Contacts without Call Record](actions/list-contacts-without-call-record.md) | GET |  |
| [Update Contact by ID](actions/update-contact-by-id.md) | PUT |  |

### Engagements

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Contact Message](actions/get-campaign-contact-message.md) | GET |  |
| [Get Message by ID](actions/get-message-by-id.md) | GET |  |
| [List Incoming Messages](actions/list-incoming-messages.md) | GET |  |
| [List Messages by Campaign](actions/list-messages-by-campaign.md) | GET |  |
| [List Messages by Contact](actions/list-messages-by-contact.md) | GET |  |
| [List Sent Messages](actions/list-sent-messages.md) | GET |  |
| [Send Contact Message](actions/send-contact-message.md) | POST |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Message Stats](actions/get-campaign-message-stats.md) | GET |  |
| [Get Collection Client Settings](actions/get-collection-client-settings.md) | GET |  |
| [Get Collection Debtor by Track ID](actions/get-collection-debtor-by-track-id.md) | GET |  |
| [Get Contact Call Record](actions/get-contact-call-record.md) | GET |  |
| [Update Collection Client Settings](actions/update-collection-client-settings.md) | PUT |  |

