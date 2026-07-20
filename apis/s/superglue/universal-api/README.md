# <img src="https://images.mindcloud.co/apps/icons/superglue_1775853591440.png" alt="Superglue logo" width="28" height="28"> Superglue: Universal API

Run tools, inspect runs, and manage end-user access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/superglue/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://superglue.cloud
- **Vendor API docs:** https://docs.superglue.cloud/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tools](actions/list-tools.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/list-tools?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Enduser

| Action | Method | Description |
| --- | --- | --- |
| [Create End User](actions/create-end-user.md) | POST |  |
| [Delete End User](actions/delete-end-user.md) | DELETE |  |
| [Get End User Details](actions/get-end-user-details.md) | GET |  |
| [List End Users](actions/list-end-users.md) | GET |  |
| [Update End User](actions/update-end-user.md) | PUT |  |

### Portalinvitation

| Action | Method | Description |
| --- | --- | --- |
| [Send Portal Invitation Email](actions/send-portal-invitation-email.md) | POST |  |

### Portallink

| Action | Method | Description |
| --- | --- | --- |
| [Generate Portal Link](actions/generate-portal-link.md) | POST |  |

### Run

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | PUT | Cancels an existing run in Superglue. |
| [Get Run Status and Metadata](actions/get-run-status-and-metadata.md) | GET | Retrieves run status and metadata from Superglue. |
| [List Runs](actions/list-runs.md) | GET | Retrieves runs from Superglue. |
| [Run Tool](actions/run-tool.md) | POST | Runs a tool in Superglue. |

### Runresult

| Action | Method | Description |
| --- | --- | --- |
| [Get Full Run Results](actions/get-full-run-results.md) | GET | Retrieves full run results from Superglue. |

### Tool

| Action | Method | Description |
| --- | --- | --- |
| [Get Tool Details](actions/get-tool-details.md) | GET | Retrieves tool details from Superglue. |
| [List Tools](actions/list-tools.md) | GET | Retrieves tools from Superglue. |

