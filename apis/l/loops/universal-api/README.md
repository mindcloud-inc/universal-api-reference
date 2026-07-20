# <img src="https://images.mindcloud.co/apps/icons/loops_1773747212434.png" alt="Loops logo" width="28" height="28"> Loops: Universal API

Manage contacts, events, and transactional emails in Loops

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loops/latest
- **Category:** Communication / Email Communications
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://loops.so
- **Vendor API docs:** https://loops.so/docs/api-reference/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Key](actions/test-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loops/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Test API Key](actions/test-api-key.md) | GET | Retrieves API key validity details from Loops. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Loops. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Loops by email or user ID. |
| [Find Contact](actions/find-contact.md) | GET | Finds a contact in Loops by email or user ID. |
| [Update Contact](actions/update-contact.md) | PUT | Updates or creates a contact in Loops. |

### Contact Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Property](actions/create-contact-property.md) | POST | Creates a new contact property in Loops. |
| [List Contact Properties](actions/list-contact-properties.md) | GET | Retrieves contact properties from your Loops account. |

### Contact Suppression

| Action | Method | Description |
| --- | --- | --- |
| [Check Contact Suppression](actions/check-contact-suppression.md) | GET | Retrieves contact suppression status from Loops. |
| [Remove Contact Suppression](actions/remove-contact-suppression.md) | DELETE | Deletes contact suppression from Loops by email or user ID. |

### Dedicated Sending Ip

| Action | Method | Description |
| --- | --- | --- |
| [List Dedicated Sending IP Addresses](actions/list-dedicated-sending-ip-addresses.md) | GET | Retrieves dedicated sending IP addresses from Loops. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Send Event](actions/send-event.md) | POST | Creates an event in Loops for a contact. |

### Mailing List

| Action | Method | Description |
| --- | --- | --- |
| [List Mailing Lists](actions/list-mailing-lists.md) | GET | Retrieves mailing lists from your Loops account. |

### Transactional Email

| Action | Method | Description |
| --- | --- | --- |
| [List Transactional Emails](actions/list-transactional-emails.md) | GET | Retrieves transactional emails from your Loops account. |
| [Send Transactional Email](actions/send-transactional-email.md) | POST | Creates a transactional email send in Loops. |

