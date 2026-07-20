# <img src="https://images.mindcloud.co/apps/icons/formcrafts_1773928503627.png" alt="Formcrafts logo" width="28" height="28"> Formcrafts: Universal API

Manage forms, responses, files, and workspaces in Formcrafts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/formcrafts/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://formcrafts.com
- **Vendor API docs:** https://formcrafts.com/help/developers/api-docs-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formcrafts/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File Content](actions/get-file-content.md) | GET | Retrieves the content of an uploaded file from Formcrafts. |
| [List Files](actions/list-files.md) | GET | Retrieves a list of uploaded files from Formcrafts. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET | Retrieves a specific form from Formcrafts. |
| [List Forms](actions/list-forms.md) | GET | Retrieves a list of forms from Formcrafts. |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Form Responses](actions/list-form-responses.md) | GET | Retrieves responses for a form from Formcrafts. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves a list of workspaces from Formcrafts. |

