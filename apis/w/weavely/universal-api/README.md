# <img src="https://images.mindcloud.co/apps/icons/67e406af05acd6cbb067951f-weavely-fav-32_1775674651754.png" alt="Weavely logo" width="28" height="28"> Weavely: Universal API

Generate AI-powered forms, collect responses, and sync data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/weavely/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.weavely.ai/
- **Vendor API docs:** https://help.weavely.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in Weavely. |
| [Generate Form](actions/generate-form.md) | POST | Creates a generated form in Weavely from a prompt. |
| [Get Form Fields](actions/get-form-fields.md) | GET | Retrieves fields from a Weavely form. |
| [Get Published Form Specification](actions/get-published-form-specification.md) | GET | Retrieves a published form specification from Weavely. |
| [List Team Forms](actions/list-team-forms.md) | GET | Retrieves forms from a Weavely team. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in Weavely. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Weavely. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook for a Weavely form. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from a Weavely form. |

