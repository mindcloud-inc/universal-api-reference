# <img src="https://images.mindcloud.co/apps/icons/cropped-rowform-favicon-final-32x32_1775164797154.png" alt="Rowform logo" width="28" height="28"> Rowform: Universal API

Build conversational forms and surveys, collect responses, and connect Rowform data to automation tools through its documented Zapier API surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rowform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rowform.io/
- **Vendor API docs:** https://help.rowform.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowform/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Rowform. |

### Form Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Responses](actions/get-form-responses.md) | GET | Retrieves form responses from Rowform. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET | Retrieves API key validation details from Rowform. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions from Rowform. |
| [Subscribe Webhook](actions/subscribe-webhook.md) | POST | Creates a webhook subscription in Rowform. |
| [Unsubscribe Webhook](actions/unsubscribe-webhook.md) | DELETE | Deletes a webhook subscription from Rowform. |

