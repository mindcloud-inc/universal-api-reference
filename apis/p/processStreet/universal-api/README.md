# <img src="https://images.mindcloud.co/apps/icons/process-street_1773413967590.png" alt="Process Street logo" width="28" height="28"> Process Street: Universal API

Manage workflows, workflow runs, tasks, and data sets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/processStreet/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.process.st/
- **Vendor API docs:** https://public-api.process.st/api/v1.1/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Authentication](actions/test-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Approval

| Action | Method | Description |
| --- | --- | --- |
| [Approve or Reject Task](actions/approve-or-reject-task.md) | PUT |  |
| [List Approvals](actions/list-approvals.md) | GET |  |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Test Authentication](actions/test-authentication.md) | GET |  |

### Data Set

| Action | Method | Description |
| --- | --- | --- |
| [List Data Sets](actions/list-data-sets.md) | GET |  |

### Data Set Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Set Record](actions/get-data-set-record.md) | GET |  |
| [List Data Set Records](actions/list-data-set-records.md) | GET |  |

### Form Field

| Action | Method | Description |
| --- | --- | --- |
| [List Form Fields](actions/list-form-fields.md) | GET |  |

### Form Field Option

| Action | Method | Description |
| --- | --- | --- |
| [List Form Field Options](actions/list-form-field-options.md) | GET |  |

### Form Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Form Field Values](actions/batch-update-form-field-values.md) | PUT |  |
| [List Task Form Field Values](actions/list-task-form-field-values.md) | GET |  |
| [List Workflow Run Form Field Values](actions/list-workflow-run-form-field-values.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET |  |
| [List Workflow Run Tasks](actions/list-workflow-run-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [List Workflows](actions/list-workflows.md) | GET |  |

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow Run](actions/create-workflow-run.md) | POST |  |
| [Delete Workflow Run](actions/delete-workflow-run.md) | DELETE |  |
| [Get Workflow Run](actions/get-workflow-run.md) | GET |  |
| [Search Workflow Runs](actions/search-workflow-runs.md) | GET |  |
| [Update Workflow Run](actions/update-workflow-run.md) | PUT |  |

### Workflow Run Assignee

| Action | Method | Description |
| --- | --- | --- |
| [Assign Workflow Run User](actions/assign-workflow-run-user.md) | PUT |  |
| [List Workflow Run Assignees](actions/list-workflow-run-assignees.md) | GET |  |
| [Unassign Workflow Run User](actions/unassign-workflow-run-user.md) | PUT |  |

