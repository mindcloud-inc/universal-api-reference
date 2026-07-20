# <img src="https://images.mindcloud.co/apps/icons/selzy_1774990143453.png" alt="Selzy logo" width="28" height="28"> Selzy: Universal API

Create campaigns, manage contacts, and track email performance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/selzy/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://selzy.com
- **Vendor API docs:** https://selzy.com/en/support/api/common/bulk-email/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contact Lists](actions/list-contact-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Campaign](actions/cancel-campaign.md) | PUT | Cancels a scheduled campaign in Selzy. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Selzy. |
| [Get Campaign Common Stats](actions/get-campaign-common-stats.md) | GET | Retrieves common campaign stats from Selzy. |
| [Get Campaign Delivery Stats](actions/get-campaign-delivery-stats.md) | GET | Retrieves campaign delivery stats from Selzy. |
| [Get Campaign Status](actions/get-campaign-status.md) | GET | Retrieves the status of a Selzy campaign. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Selzy. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Exclude Contact](actions/exclude-contact.md) | PUT | Excludes a contact from one or more Selzy lists. |
| [Export Contacts](actions/export-contacts.md) | GET | Exports contacts from Selzy. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Selzy. |
| [Get Contact Count](actions/get-contact-count.md) | GET | Retrieves the contact count for a Selzy list. |
| [Get Total Contact Count](actions/get-total-contact-count.md) | GET | Retrieves the total contact count for a Selzy user. |
| [Import Contacts](actions/import-contacts.md) | POST | Imports contacts into Selzy. |
| [Subscribe Contact](actions/subscribe-contact.md) | POST | Subscribes a contact to one or more Selzy lists. |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | PUT | Marks a contact as unsubscribed in Selzy. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Field](actions/create-contact-field.md) | POST | Creates a new contact field in Selzy. |
| [List Contact Fields](actions/list-contact-fields.md) | GET | Retrieves contact fields from Selzy. |
| [Update Contact Field](actions/update-contact-field.md) | PUT | Updates an existing contact field in Selzy. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Check Email](actions/check-email.md) | GET | Retrieves the delivery status of a Selzy email. |
| [Send Email](actions/send-email.md) | POST | Sends a single email through Selzy. |
| [Send Test Email](actions/send-test-email.md) | POST | Sends a test email from a Selzy message. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in Selzy. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from Selzy. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Selzy. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in Selzy. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Message](actions/create-email-message.md) | POST | Creates a new email message in Selzy. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from Selzy. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from Selzy. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from Selzy. |
| [Update Email Message](actions/update-email-message.md) | PUT | Updates an existing email message in Selzy. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Selzy. |

