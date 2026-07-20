# <img src="https://images.mindcloud.co/apps/icons/logo-ligne-1600x340-orange_1781642048949.png" alt="Conexteo logo" width="28" height="28"> Conexteo: Universal API

Conexteo: Send SMS and RCS campaigns, manage contacts, track replies

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/conexteo/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://conexteo.com
- **Vendor API docs:** https://developers.conexteo.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contact Lists](actions/list-contact-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts](actions/add-contacts.md) | POST | Creates contacts in Conexteo. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Conexteo. |
| [List Contacts In Contact List](actions/list-contacts-in-contact-list.md) | GET | Finds contacts in a Conexteo contact list. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Conexteo. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a contact list in Conexteo. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from Conexteo. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list from Conexteo. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Finds contact lists in Conexteo. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in Conexteo. |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves account credits from Conexteo. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Message History](actions/list-message-history.md) | GET | Finds message history in Conexteo. |
| [Send Dynamic SMS](actions/send-dynamic-sms.md) | POST | Creates a dynamic SMS message in Conexteo. |
| [Send Manual SMS](actions/send-manual-sms.md) | POST | Creates a manual SMS message in Conexteo. |
| [Send SMS To Contact Lists](actions/send-sms-to-contact-lists.md) | POST | Creates an SMS message for Conexteo contact lists. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a message template in Conexteo. |
| [Get Model](actions/get-model.md) | GET | Retrieves a message template from Conexteo. |
| [List Models](actions/list-models.md) | GET | Finds message templates in Conexteo. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Manual Stop](actions/create-manual-stop.md) | POST | Creates a manual stop in Conexteo. |
| [List All Message Replies](actions/list-all-message-replies.md) | GET | Finds all message replies in Conexteo. |
| [List Message Replies](actions/list-message-replies.md) | GET | Finds message replies in Conexteo. |
| [List RCS Models](actions/list-rcs-models.md) | GET | Finds RCS templates in Conexteo. |

### Stop

| Action | Method | Description |
| --- | --- | --- |
| [Delete Stop](actions/delete-stop.md) | DELETE | Deletes an existing stop from Conexteo. |
| [List Stops](actions/list-stops.md) | GET | Finds stopped subscribers in Conexteo. |

