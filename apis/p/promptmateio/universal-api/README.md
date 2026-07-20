# <img src="https://images.mindcloud.co/apps/icons/promptmateio_1774987923406.png" alt="Promptmate.io logo" width="28" height="28"> Promptmate.io: Universal API

Promptmate.io API for templates, apps, app jobs, projects, webhooks, reference data, and user info.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/promptmateio/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://promptmate.io
- **Vendor API docs:** https://apidoc.promptmate.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Result Rows](actions/get-app-result-rows.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/get-app-result-rows?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### App

| Action | Method | Description |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | GET |  |
| [Use Template](actions/use-template.md) | POST |  |

### App Job

| Action | Method | Description |
| --- | --- | --- |
| [Create App Job](actions/create-app-job.md) | POST |  |

### App Result

| Action | Method | Description |
| --- | --- | --- |
| [Get App Result Rows](actions/get-app-result-rows.md) | GET |  |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET |  |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Languages](actions/list-languages.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Information](actions/get-user-information.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

