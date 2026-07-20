# <img src="https://images.mindcloud.co/apps/icons/eztexting-logo_1773343203836.jpeg" alt="EZ Texting logo" width="28" height="28"> EZ Texting: Universal API

SMS marketing and messaging for contacts, groups, conversations, media, reports, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eZTexting/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eztexting.com/
- **Vendor API docs:** https://developers.eztexting.com/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit Balance](actions/get-credit-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts to Contact Group](actions/add-contacts-to-contact-group.md) | PUT | Adds contacts to a contact group in EZ Texting. |
| [Create Contact Group](actions/create-contact-group.md) | POST | Creates a contact group in EZ Texting. |
| [Create Media File](actions/create-media-file.md) | POST | Creates a media file in EZ Texting. |
| [Create Message](actions/create-message.md) | POST | Creates a message in EZ Texting. |
| [Create or Update a Batch of Contacts](actions/create-or-update-a-batch-of-contacts.md) | PUT | Creates or updates multiple contacts in EZ Texting. |
| [Create or Update Contact](actions/create-or-update-contact.md) | PUT | Creates or updates a contact in EZ Texting. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in EZ Texting. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from EZ Texting. |
| [Delete Contact Group](actions/delete-contact-group.md) | DELETE | Deletes a contact group from EZ Texting. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from EZ Texting. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from EZ Texting by phone number. |
| [Get Contact Group](actions/get-contact-group.md) | GET | Retrieves a contact group from EZ Texting. |
| [Get Credit Balance](actions/get-credit-balance.md) | GET | Retrieves account credit balance from EZ Texting. |
| [Get Media File](actions/get-media-file.md) | GET | Retrieves a media file from EZ Texting. |
| [List Contact Groups](actions/list-contact-groups.md) | GET | Retrieves contact groups from EZ Texting. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from EZ Texting. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from EZ Texting. |
| [List Media Files](actions/list-media-files.md) | GET | Retrieves media files from EZ Texting. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from EZ Texting. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from EZ Texting. |
| [Remove Contacts from Contact Group](actions/remove-contacts-from-contact-group.md) | PUT | Removes contacts from a contact group in EZ Texting. |
| [Update Contact Group](actions/update-contact-group.md) | PUT | Updates a contact group in EZ Texting. |

