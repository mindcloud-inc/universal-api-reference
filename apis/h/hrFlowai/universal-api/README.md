# <img src="https://images.mindcloud.co/apps/icons/clip-path-group-5_1781898776824.png" alt="HrFlow.ai logo" width="28" height="28"> HrFlow.ai: Universal API

Search, parse, enrich, and manage candidate and job data with HrFlow.ai's recruiting API platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hrFlowai/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hrflow.ai/
- **Vendor API docs:** https://developers.hrflow.ai/docs/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Credentials](actions/validate-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hrFlowai/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | GET | Retrieves boards for the authenticated HrFlow.ai team. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves sources for the authenticated HrFlow.ai team. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Validate Credentials](actions/validate-credentials.md) | GET | Verifies HrFlow.ai API credentials and retrieves team details. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows for the authenticated HrFlow.ai team. |

