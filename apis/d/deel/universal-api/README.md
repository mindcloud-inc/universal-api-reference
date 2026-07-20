# <img src="https://images.mindcloud.co/apps/icons/unnamed_1774036300454.png" alt="Deel logo" width="28" height="28"> Deel: Universal API

Deel helps companies hire, manage, and pay global teams. This app wraps Deel's public API for contractor operations and workforce workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/deel/latest
- **Category:** Human Resources / HRIS
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.deel.com
- **Vendor API docs:** https://developer.deel.com/api/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contracts](actions/list-contracts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deel/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Adjustment Categories](actions/list-adjustment-categories.md) | GET | Retrieves the adjustment categories from Deel. |

### Contract Amendments

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Amendment](actions/create-contract-amendment.md) | POST | Creates a contract amendment in Deel. |
| [List Contract Amendments](actions/list-contract-amendments.md) | GET | Retrieves the amendments for a contract from Deel. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Document](actions/create-contract-document.md) | POST | Attaches a document to a contract in Deel. |
| [Create Contract Invitation](actions/create-contract-invitation.md) | POST | Sends a contract invitation to a worker in Deel. |
| [Create Contract Signature](actions/create-contract-signature.md) | POST | Signs a contract for the client in Deel. |
| [Create IC Contract](actions/create-ic-contract.md) | POST | Creates a new IC contract in Deel. |
| [Get Contract](actions/get-contract.md) | GET | Retrieves the details of a contract from Deel. |
| [Get Contract Invitations](actions/get-contract-invitations.md) | GET |  |
| [Get Contract Invite](actions/get-contract-invite.md) | GET | Retrieves the contract invite link from Deel. |
| [List Contract Payment Cycles](actions/list-contract-payment-cycles.md) | GET | Retrieves contract payment cycles from Deel. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves a paginated list of contracts from Deel. |
| [Update IC Contract](actions/update-ic-contract.md) | PUT | Updates an existing IC contract in Deel. |

### Milestones

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Milestone](actions/create-contract-milestone.md) | POST | Creates a contract milestone in Deel. |
| [Delete Contract Milestone](actions/delete-contract-milestone.md) | DELETE | Deletes an existing contract milestone from Deel. |
| [Get Contract Milestone by ID](actions/get-contract-milestone-by-id.md) | GET | Retrieves a contract milestone from Deel by ID. |
| [List Contract Milestones](actions/list-contract-milestones.md) | GET | Retrieves milestones for a contract from Deel. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Task](actions/create-contract-task.md) | POST | Creates a contract task in Deel. |
| [Create Contract Task Review](actions/create-contract-task-review.md) | POST | Creates a contract task review in Deel. |
| [Delete Contract Task](actions/delete-contract-task.md) | DELETE | Deletes an existing contract task from Deel. |
| [List Contract Tasks](actions/list-contract-tasks.md) | GET | Retrieves tasks for a contract from Deel. |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet](actions/create-timesheet.md) | POST | Creates a new timesheet in Deel. |
| [Create Timesheet Review](actions/create-timesheet-review.md) | POST | Creates a timesheet review in Deel. |
| [Get Timesheet by ID](actions/get-timesheet-by-id.md) | GET | Retrieves a timesheet from Deel by ID. |
| [List Contract Timesheets](actions/list-contract-timesheets.md) | GET | Retrieves timesheets for a contract from Deel. |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves a paginated list of timesheets from Deel. |
| [Update Timesheet](actions/update-timesheet.md) | PUT | Updates an existing timesheet in Deel. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Adjustment](actions/create-contract-adjustment.md) | POST | Creates a contract adjustment in Deel. |
| [Create Invoice Adjustment Review](actions/create-invoice-adjustment-review.md) | POST | Creates an invoice adjustment review in Deel. |
| [Delete Contract Adjustment](actions/delete-contract-adjustment.md) | DELETE | Deletes an existing contract adjustment from Deel. |
| [Delete Invoice Adjustment](actions/delete-invoice-adjustment.md) | DELETE | Deletes an existing invoice adjustment from Deel. |
| [Get Contract Adjustment](actions/get-contract-adjustment.md) | GET | Retrieves a contract adjustment from Deel. |
| [Get Invoice Adjustment by ID](actions/get-invoice-adjustment-by-id.md) | GET | Retrieves an invoice adjustment from Deel by ID. |
| [List Contract Adjustments](actions/list-contract-adjustments.md) | GET | Retrieves adjustments for a contract from Deel. |
| [List Contract Invoice Adjustments](actions/list-contract-invoice-adjustments.md) | GET | Retrieves invoice adjustments for a contract from Deel. |
| [List Invoice Adjustments](actions/list-invoice-adjustments.md) | GET | Retrieves the invoice adjustments from Deel. |
| [Update Contract Adjustment](actions/update-contract-adjustment.md) | PUT | Updates an existing contract adjustment in Deel. |

