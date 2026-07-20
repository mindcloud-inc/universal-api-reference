# <img src="https://images.mindcloud.co/apps/icons/idq-qv2pih-t-logos_1775059663672.jpeg" alt="AvoSMS logo" width="28" height="28"> AvoSMS: Universal API

Send SMS campaigns and manage contacts, templates, and responses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/avoSMS/latest
- **Category:** Marketing
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.avosms.com/en
- **Vendor API docs:** https://www.avosms.com/en/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Balance](actions/get-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Account Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET | Retrieves your account balance from AvoSMS. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | POST | Creates a new contact in AvoSMS. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from AvoSMS. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in AvoSMS. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in AvoSMS. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from AvoSMS. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list and its contacts from AvoSMS. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from AvoSMS. |
| [Rename Contact List](actions/rename-contact-list.md) | PUT | Updates an existing contact list in AvoSMS. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [List Available Destinations](actions/list-available-destinations.md) | GET | Retrieves available destinations from AvoSMS. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender](actions/create-sender.md) | POST | Creates a new sender in AvoSMS. |
| [Delete Sender](actions/delete-sender.md) | DELETE | Deletes an existing sender from AvoSMS. |
| [List Senders](actions/list-senders.md) | GET | Retrieves senders from AvoSMS. |

### Sms

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends an SMS with AvoSMS. |

### Sms Response

| Action | Method | Description |
| --- | --- | --- |
| [List SMS Responses](actions/list-sms-responses.md) | GET | Retrieves SMS responses from AvoSMS. |

### Sms Template

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Template](actions/create-sms-template.md) | POST | Creates a new SMS template in AvoSMS. |
| [Delete SMS Template](actions/delete-sms-template.md) | DELETE | Deletes an existing SMS template from AvoSMS. |
| [Get SMS Template](actions/get-sms-template.md) | GET | Retrieves an SMS template from AvoSMS. |
| [List SMS Templates](actions/list-sms-templates.md) | GET | Retrieves SMS templates from AvoSMS. |
| [Update SMS Template](actions/update-sms-template.md) | PUT | Updates an existing SMS template in AvoSMS. |

