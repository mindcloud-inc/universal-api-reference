# <img src="https://images.mindcloud.co/apps/icons/customersai_1774023035070.png" alt="Customers.ai logo" width="28" height="28"> Customers.ai: Universal API

Identify website visitors and enrich customer data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/customersai/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://customers.ai
- **Vendor API docs:** https://customers.ai/help/l/en/category/doq3ewxla3-public-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contact IDs](actions/list-contact-ids.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customersai/latest/actions/list-contact-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates an SMS contact in Customers.ai, or updates an existing match. |
| [List Contact IDs](actions/list-contact-ids.md) | GET |  |
| [Opt-In SMS Contact](actions/opt-in-sms-contact.md) | POST | Opts a new SMS contact into a promoter in Customers.ai. |
| [Send Dialogue](actions/send-dialogue.md) | PUT | Sends a dialogue to a contact in Customers.ai. |
| [Send JSON Message](actions/send-json-message.md) | PUT | Sends a JSON message to a contact in Customers.ai. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Customers.ai. |

### Promoter

| Action | Method | Description |
| --- | --- | --- |
| [List Promoters](actions/list-promoters.md) | GET | Lists active send-to-messenger promoters in Customers.ai. |

