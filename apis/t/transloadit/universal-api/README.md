# <img src="https://images.mindcloud.co/apps/icons/transloadit_1774617560885.png" alt="Transloadit logo" width="28" height="28"> Transloadit: Universal API

Transloadit is a file and media processing platform for uploads, transformations, encoding, and delivery through its API-driven Assembly workflow.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/transloadit/latest
- **Category:** Content & Files / Storage
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://transloadit.com
- **Vendor API docs:** https://transloadit.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assemblies](actions/list-assemblies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/list-assemblies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Assembly

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Assembly](actions/cancel-assembly.md) | DELETE | Cancels a running assembly in Transloadit. |
| [Create Assembly](actions/create-assembly.md) | POST | Creates a new assembly in Transloadit. |
| [List Assemblies](actions/list-assemblies.md) | GET | Retrieves a list of assemblies from Transloadit. |
| [Replay Assembly](actions/replay-assembly.md) | POST | Replays an existing assembly in Transloadit. |
| [Retrieve Assembly Status](actions/retrieve-assembly-status.md) | GET | Retrieves an assembly status from Transloadit. |

### Assembly Notification Replay

| Action | Method | Description |
| --- | --- | --- |
| [Replay Assembly Notification](actions/replay-assembly-notification.md) | POST | Replays an assembly notification in Transloadit. |

### Monthly Bill

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a month's bill](actions/retrieve-months-bill.md) | GET | Retrieves a monthly bill from Transloadit. |

### Queue Job Slots

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve currently used priority job slots](actions/retrieve-priority-job-slots.md) | GET | Retrieves currently used priority job slots from Transloadit. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Transloadit. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Transloadit. |
| [Edit Template](actions/edit-template.md) | PUT | Updates an existing template in Transloadit. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from Transloadit. |
| [Retrieve Template](actions/retrieve-template.md) | GET | Retrieves a template by ID from Transloadit. |

### Template Credential

| Action | Method | Description |
| --- | --- | --- |
| [Create Template Credential](actions/create-template-credential.md) | POST | Creates a new template credential in Transloadit. |
| [Delete Template Credential](actions/delete-template-credential.md) | DELETE | Deletes an existing template credential from Transloadit. |
| [Edit Template Credential](actions/edit-template-credential.md) | PUT | Updates an existing template credential in Transloadit. |
| [List Template Credentials](actions/list-template-credentials.md) | GET | Retrieves a list of template credentials from Transloadit. |
| [Retrieve Template Credential](actions/retrieve-template-credential.md) | GET | Retrieves a template credential from Transloadit. |

