# <img src="https://images.mindcloud.co/apps/icons/image-2843-vectorized_1777572012208.png" alt="MindCloud logo" width="28" height="28"> MindCloud: Universal API

Manage MindCloud workflows, runs, connections, members, roles, environments, API keys, usage, and Universal API metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mindCloud/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mindcloud.co
- **Vendor API docs:** https://mindcloud.co/docs/api/rest/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST |  |
| [List API Keys](actions/list-api-keys.md) | GET |  |
| [Revoke API Key](actions/revoke-api-key.md) | DELETE |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Platform Companies](actions/list-platform-companies.md) | GET |  |
| [Update Company](actions/update-company.md) | PUT |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Delete Connection](actions/delete-connection.md) | DELETE |  |
| [Get Connection](actions/get-connection.md) | GET |  |
| [List Connections](actions/list-connections.md) | GET |  |
| [Test Connection](actions/test-connection.md) | GET |  |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [List Environments](actions/list-environments.md) | GET |  |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Invite Members](actions/invite-members.md) | POST |  |
| [List Members](actions/list-members.md) | GET |  |
| [Remove Member](actions/remove-member.md) | DELETE |  |
| [Update Member Role](actions/update-member-role.md) | PUT |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST |  |
| [Delete Role](actions/delete-role.md) | DELETE |  |
| [Get Role](actions/get-role.md) | GET |  |
| [List Roles](actions/list-roles.md) | GET |  |
| [Update Role](actions/update-role.md) | PUT |  |

### Universal Action

| Action | Method | Description |
| --- | --- | --- |
| [Get Universal Action](actions/get-universal-action.md) | GET |  |
| [List Universal Actions](actions/list-universal-actions.md) | GET |  |
| [Run Universal Action](actions/run-universal-action.md) | POST |  |

### Universal App

| Action | Method | Description |
| --- | --- | --- |
| [List Universal Apps](actions/list-universal-apps.md) | GET |  |

### Usage Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Usage](actions/get-daily-usage.md) | GET |  |
| [Get Usage](actions/get-usage.md) | GET |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST |  |
| [Delete Workflow](actions/delete-workflow.md) | DELETE |  |
| [Duplicate Workflow](actions/duplicate-workflow.md) | POST |  |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |
| [Update Workflow](actions/update-workflow.md) | PUT |  |

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Run](actions/cancel-run.md) | PUT |  |
| [Get Run](actions/get-run.md) | GET |  |
| [List Workflow Runs](actions/list-workflow-runs.md) | GET |  |
| [Run Workflow](actions/run-workflow.md) | POST |  |

### Workflow Run Operation

| Action | Method | Description |
| --- | --- | --- |
| [List Run Operations](actions/list-run-operations.md) | GET |  |

### Workflow Run Step

| Action | Method | Description |
| --- | --- | --- |
| [Get Run Step](actions/get-run-step.md) | GET |  |
| [List Run Steps](actions/list-run-steps.md) | GET |  |

### Workflow Usage Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Usage](actions/get-workflow-usage.md) | GET |  |

