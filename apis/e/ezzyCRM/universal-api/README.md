# <img src="https://images.mindcloud.co/apps/icons/ezzy-crm_1774977488849.png" alt="EzzyCRM logo" width="28" height="28"> EzzyCRM: Universal API

Manage leads, pipelines, stages, and CRM users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ezzyCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ezzycrm.com
- **Vendor API docs:** https://ezzycrm.com/api/GetApiDocument.aspx

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Update Lead Assignee](actions/update-lead-assignee.md) | PUT |  |
| [Update Lead Stage](actions/update-lead-stage.md) | PUT |  |
| [Update Lead Status](actions/update-lead-status.md) | PUT |  |

### Lost Reason

| Action | Method | Description |
| --- | --- | --- |
| [List Lost Reasons](actions/list-lost-reasons.md) | GET |  |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET |  |

### Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Stages](actions/list-stages.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

