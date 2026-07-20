# <img src="https://images.mindcloud.co/apps/icons/plum-docs_1774904487915.png" alt="PlumDocs logo" width="28" height="28"> PlumDocs: Universal API

Generate and manage documents from Google Docs templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/plumDocs/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://plumdocs.com/
- **Vendor API docs:** https://plumdocs.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plumDocs/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Generate Document](actions/generate-document.md) | POST | Generates a document from a PlumDocs workflow. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves authenticated user details from PlumDocs. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Fields](actions/get-workflow-fields.md) | GET | Retrieves workflow field definitions from PlumDocs. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves a list of workflows from PlumDocs. |

