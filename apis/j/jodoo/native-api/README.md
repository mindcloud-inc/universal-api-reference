# Jodoo: Native API Reference

A consolidated summary of Jodoo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://help.jodoo.com/en/collections/11230973-api
- **API base URL:** `https://api.jodoo.com/api/v5`

## Authentication

### API Key

Use a Jodoo Open Platform API key with bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.jodoo.com/en/articles/9991900-api-key)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | `POST /corp/user/create` | [docs](https://help.jodoo.com/en/articles/9992456-member-adding-api) |
| [Create Record](actions/create-record.md) | `POST /app/entry/data/create` | [docs](https://help.jodoo.com/en/articles/9992387-single-record-creation-api) |
| [Create Records](actions/create-records.md) | `POST /app/entry/data/batch_create` | [docs](https://help.jodoo.com/en/articles/9992388-multiple-records-creation-api) |
| [Delete Record](actions/delete-record.md) | `POST /app/entry/data/delete` | [docs](https://help.jodoo.com/en/articles/10335116-single-record-deletion-api) |
| [Delete Records](actions/delete-records.md) | `POST /app/entry/data/batch_delete` | [docs](https://help.jodoo.com/en/articles/9992415-multiple-records-deletion-api) |
| [Get Approval Comments](actions/get-approval-comments.md) | `POST https://api.jodoo.com/api/v1/app/:app_id/entry/:entry_id/data/:data_id/approval_comments` | [docs](https://help.jodoo.com/en/articles/9992419-approval-comments-query-api) |
| [Get Member](actions/get-member.md) | `POST /corp/user/get` | [docs](https://help.jodoo.com/en/articles/9992455-member-information-query-api) |
| [Get Record](actions/get-record.md) | `POST /app/entry/data/get` | [docs](https://help.jodoo.com/en/articles/9992384-single-record-query-api) |
| [Get Workflow Instance](actions/get-workflow-instance.md) | `POST https://api.jodoo.com/api/v6/workflow/instance/get` | [docs](https://help.jodoo.com/en/articles/9992396-workflow-instances-query-api) |
| [Get Workflow Instance Logs](actions/get-workflow-instance-logs.md) | `POST https://api.jodoo.com/api/v1/workflow/instance/logs` | [docs](https://help.jodoo.com/en/articles/9992397-workflow-instance-logs-query-api) |
| [List Apps](actions/list-apps.md) | `POST /app/list` | [docs](https://help.jodoo.com/en/articles/9992363-user-app-query-api) |
| [List Department Members](actions/list-department-members.md) | `POST /corp/department/user/list` | [docs](https://help.jodoo.com/en/articles/9992441-member-retrieval-recursively-api) |
| [List Departments](actions/list-departments.md) | `POST /corp/department/list` | [docs](https://help.jodoo.com/en/articles/9992464-department-lists-retrieval-recursively) |
| [List Forms](actions/list-forms.md) | `POST /app/entry/list` | [docs](https://help.jodoo.com/en/articles/9992378-user-form-query-api) |
| [List Records](actions/list-records.md) | `POST /app/entry/data/list` | [docs](https://help.jodoo.com/en/articles/9992385-multiple-records-query-api) |
| [List Workflow Tasks](actions/list-workflow-tasks.md) | `POST https://api.jodoo.com/api/v4/workflow/task/list` | [docs](https://help.jodoo.com/en/articles/9992446-workflow-tasks-query-api) |
| [Reject Workflow Task](actions/reject-workflow-task.md) | `POST https://api.jodoo.com/api/v1/workflow/task/reject` | [docs](https://help.jodoo.com/en/articles/11274841-workflow-task-rejection-api) |
| [Return Workflow Task](actions/return-workflow-task.md) | `POST https://api.jodoo.com/api/v1/workflow/task/rollback` | [docs](https://help.jodoo.com/en/articles/9992426-workflow-tasks-return-api) |
| [Submit Workflow Task](actions/submit-workflow-task.md) | `POST https://api.jodoo.com/api/v1/workflow/task/approve` | [docs](https://help.jodoo.com/en/articles/9992447-workflow-tasks-submit-api) |
| [Transfer Workflow Task](actions/transfer-workflow-task.md) | `POST https://api.jodoo.com/api/v1/workflow/task/transfer` | [docs](https://help.jodoo.com/en/articles/9992428-workflow-tasks-transfer-api) |
| [Update Member](actions/update-member.md) | `POST /corp/user/update` | [docs](https://help.jodoo.com/en/articles/9992457-member-update-api) |
| [Update Record](actions/update-record.md) | `POST /app/entry/data/update` | [docs](https://help.jodoo.com/en/articles/9992411-single-record-update-api) |
| [Update Records](actions/update-records.md) | `POST /app/entry/data/batch_update` | [docs](https://help.jodoo.com/en/articles/10335100-multiple-records-update-api) |
| [Withdraw Workflow Task](actions/withdraw-workflow-task.md) | `POST https://api.jodoo.com/api/v1/workflow/task/revoke` | [docs](https://help.jodoo.com/en/articles/9992452-workflow-tasks-withdraw-api) |
