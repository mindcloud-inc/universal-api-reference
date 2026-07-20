# <img src="https://images.mindcloud.co/apps/icons/activemerge_1775072919335.png" alt="ActiveMerge logo" width="28" height="28"> ActiveMerge: Universal API

ActiveMerge API for generating and merging documents/images from templates, listing templates/workflows/files, and retrieving generated outputs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activeMerge/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://activemerge.com
- **Vendor API docs:** https://app.activemerge.com/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Credits](actions/get-user-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeMerge/latest/actions/get-user-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Generate Document](actions/generate-document.md) | POST | Generates a document from a template in ActiveMerge. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET | Retrieves files and folders for the authenticated user from ActiveMerge. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Image Templates](actions/list-image-templates.md) | GET | Retrieves image templates for the authenticated user from ActiveMerge. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates for the authenticated user from ActiveMerge. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Credits](actions/get-user-credits.md) | GET | Retrieves remaining user credits from ActiveMerge. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Generate Workflow Documents](actions/generate-workflow-documents.md) | POST | Generates documents from a workflow in ActiveMerge. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows for the authenticated user from ActiveMerge. |

