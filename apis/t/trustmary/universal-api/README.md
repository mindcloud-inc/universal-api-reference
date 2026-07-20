# <img src="https://images.mindcloud.co/apps/icons/trustmary_1773937356062.png" alt="Trustmary logo" width="28" height="28"> Trustmary: Universal API

Trustmary Integration API for contacts, surveys, reviews, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trustmary/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trustmary.com
- **Vendor API docs:** https://help.trustmary.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test API Key](actions/test-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trustmary/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Api Test Result

| Action | Method | Description |
| --- | --- | --- |
| [Test API Key](actions/test-api-key.md) | GET | Retrieves API key test results from Trustmary. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Contact](actions/create-or-update-contact.md) | POST | Finds a contact by email in Trustmary, or creates one if missing. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Trustmary. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Trustmary. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from Trustmary. |

### Embed

| Action | Method | Description |
| --- | --- | --- |
| [List Embeds](actions/list-embeds.md) | GET | Retrieves embeds from Trustmary. |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [List Experiments](actions/list-experiments.md) | GET | Retrieves experiments from Trustmary. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [Get Survey Information](actions/get-survey-information.md) | GET | Retrieves survey details from Trustmary. |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves surveys from Trustmary. |

### Survey Response

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Responses](actions/list-survey-responses.md) | GET | Retrieves responses for a survey from Trustmary. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Trustmary. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Trustmary. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Trustmary. |

### Webhook Example

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Example Payload](actions/get-webhook-example-payload.md) | GET | Retrieves example webhook payloads from Trustmary. |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves widgets from Trustmary. |

