# <img src="https://images.mindcloud.co/apps/icons/pipefile_1774464928689.png" alt="Pipefile logo" width="28" height="28"> Pipefile: Universal API

Collect, send, and manage client document requests

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pipefile/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pipefile.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipefile/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Pipefile. |
| [List Contacts](actions/list-contacts.md) | GET | Finds contacts in Pipefile by optional filters. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Pipefile. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhook endpoints from Pipefile. |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

