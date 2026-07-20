# <img src="https://images.mindcloud.co/apps/icons/idsr-s2w3t-e-1773857484734_1773857491971.jpeg" alt="Signaturit logo" width="28" height="28"> Signaturit: Universal API

Send, sign, and manage agreements and certified messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signaturit/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.signaturit.com/
- **Vendor API docs:** https://docs.signaturit.com/api/latest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Certified Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Certified Email](actions/get-certified-email.md) | GET | Retrieves a certified email from Signaturit. |
| [List Certified Emails](actions/list-certified-emails.md) | GET | Retrieves certified emails from Signaturit. |

### Certified Sms

| Action | Method | Description |
| --- | --- | --- |
| [List Certified SMS](actions/list-certified-sms.md) | GET | Retrieves certified SMS messages from Signaturit. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Signaturit. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Signaturit. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Signaturit. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Signaturit. |

### Credit

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves account credits from Signaturit. |

### Event Hook

| Action | Method | Description |
| --- | --- | --- |
| [List Event Hooks](actions/list-event-hooks.md) | GET | Retrieves event hooks from Signaturit. |

### Signature

| Action | Method | Description |
| --- | --- | --- |
| [Get Signature](actions/get-signature.md) | GET | Retrieves a signature from Signaturit. |
| [List Signatures](actions/list-signatures.md) | GET | Retrieves signatures from Signaturit. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Signaturit. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes an existing subscription from Signaturit. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Signaturit. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Signaturit. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Signaturit. |
| [List Templates V4](actions/list-templates-v4.md) | GET | Retrieves templates from Signaturit V4 API. |

