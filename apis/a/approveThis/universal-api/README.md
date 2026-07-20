# <img src="https://images.mindcloud.co/apps/icons/approve-this_1776891621245.png" alt="ApproveThis logo" width="28" height="28"> ApproveThis: Universal API

Manage approval templates, workflows, and approval decisions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/approveThis/latest
- **Category:** Productivity / Project Management
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.approvethis.com
- **Vendor API docs:** https://app.approvethis.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workflows](actions/list-workflows.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/approveThis/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new approval template in ApproveThis. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an approval template from ApproveThis by slug. |
| [Generate Template](actions/generate-template.md) | POST | Creates an approval template from JSON data in ApproveThis. |
| [Get Template](actions/get-template.md) | GET | Retrieves an approval template from ApproveThis by slug. |
| [List Template Fields](actions/list-template-fields.md) | GET | Retrieves fields for an approval template in ApproveThis. |
| [List Templates](actions/list-templates.md) | GET | Retrieves approval templates from your ApproveThis workspace. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing approval template in ApproveThis. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a workflow from an ApproveThis template. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from ApproveThis by ID. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves approval workflows from your ApproveThis workspace. |

