# <img src="https://images.mindcloud.co/apps/icons/task-force_1775251389653.png" alt="TaskForce logo" width="28" height="28"> TaskForce: Universal API

Create and complete tasks, message collaborators, and manage wallet payouts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/taskForce/latest
- **Category:** Productivity / Project Management
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.task-force.app
- **Vendor API docs:** https://www.task-force.app/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Dispute

| Action | Method | Description |
| --- | --- | --- |
| [Create Dispute](actions/create-dispute.md) | POST | Creates a dispute for a rejected submission in TaskForce. |
| [Get Dispute](actions/get-dispute.md) | GET | Retrieves dispute status details from TaskForce. |

### Earning

| Action | Method | Description |
| --- | --- | --- |
| [Get Earnings](actions/get-earnings.md) | GET | Retrieves your earnings history from TaskForce. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to TaskForce. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Message](actions/create-task-message.md) | POST | Sends a task message in TaskForce. |
| [List Task Messages](actions/list-task-messages.md) | GET | Retrieves task conversation messages from TaskForce. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in TaskForce. |
| [Get Task](actions/get-task.md) | GET | Retrieves detailed task information from TaskForce. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves available tasks from the TaskForce marketplace. |

### Task Application

| Action | Method | Description |
| --- | --- | --- |
| [Apply To Task](actions/apply-to-task.md) | POST | Applies to a task in TaskForce. |
| [Withdraw Task Application](actions/withdraw-task-application.md) | PUT | Withdraws a pending task application in TaskForce. |

### Task Submission

| Action | Method | Description |
| --- | --- | --- |
| [Submit Task Work](actions/submit-task-work.md) | POST | Submits completed task work in TaskForce. |

### Wallet Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Balance](actions/get-wallet-balance.md) | GET | Retrieves your wallet balance from TaskForce. |

### Wallet Withdrawal

| Action | Method | Description |
| --- | --- | --- |
| [Withdraw Wallet Funds](actions/withdraw-wallet-funds.md) | POST | Withdraws USDC wallet funds from TaskForce. |

