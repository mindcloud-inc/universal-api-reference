# <img src="https://images.mindcloud.co/apps/icons/jodoo_1774459799577.png" alt="Jodoo logo" width="28" height="28"> Jodoo: Universal API

Manage Jodoo apps, forms, records, workflows, and contacts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jodoo/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.jodoo.com
- **Vendor API docs:** https://help.jodoo.com/en/collections/11230973-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Approval Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Approval Comments](actions/get-approval-comments.md) | GET |  |

### Apps

| Action | Method | Description |
| --- | --- | --- |
| [List Apps](actions/list-apps.md) | GET |  |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET |  |

### Members

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST |  |
| [Get Member](actions/get-member.md) | GET |  |
| [List Department Members](actions/list-department-members.md) | GET |  |
| [Update Member](actions/update-member.md) | PUT |  |

### Records

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST |  |
| [Create Records](actions/create-records.md) | POST |  |
| [Delete Record](actions/delete-record.md) | DELETE |  |
| [Delete Records](actions/delete-records.md) | DELETE |  |
| [Get Record](actions/get-record.md) | GET |  |
| [List Records](actions/list-records.md) | GET |  |
| [Update Record](actions/update-record.md) | PUT |  |
| [Update Records](actions/update-records.md) | PUT |  |

### Workflow Instances

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Instance](actions/get-workflow-instance.md) | GET |  |

### Workflow Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Instance Logs](actions/get-workflow-instance-logs.md) | GET |  |

### Workflow Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Tasks](actions/list-workflow-tasks.md) | GET |  |
| [Reject Workflow Task](actions/reject-workflow-task.md) | PUT |  |
| [Return Workflow Task](actions/return-workflow-task.md) | PUT |  |
| [Submit Workflow Task](actions/submit-workflow-task.md) | PUT |  |
| [Transfer Workflow Task](actions/transfer-workflow-task.md) | PUT |  |
| [Withdraw Workflow Task](actions/withdraw-workflow-task.md) | PUT |  |

