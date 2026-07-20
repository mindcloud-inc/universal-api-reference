# <img src="https://images.mindcloud.co/apps/icons/image-2842-vectorized_1777479741230.png" alt="AidaForm logo" width="28" height="28"> AidaForm: Universal API

Create forms, collect responses, and accept online payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aidaForm/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aidaform.com
- **Vendor API docs:** https://app.swaggerhub.com/apis/aidaform/AidaForm/1.0.1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aidaForm/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from your AidaForm account. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Responses](actions/list-responses.md) | GET | Retrieves form responses from AidaForm by form ID. |

