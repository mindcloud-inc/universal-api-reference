# Deel: Native API Reference

A consolidated summary of Deel's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developer.deel.com/api/introduction
- **API base URL:** `https://api.letsdeel.com/rest/v2`

## Authentication

### API Token

Connect Deel with an API token.

### Credentials

- **API Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.deel.com/docs/api-tokens-1)

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contract Adjustment](actions/create-contract-adjustment.md) | `POST /adjustments` | [docs](https://developer.deel.com/api/endpoints/adjustments/create-contract-adjustment) |
| [Create Contract Amendment](actions/create-contract-amendment.md) | `POST /contracts/:contract_id/amendments` | [docs](https://developer.deel.com/api/endpoints/contractor-amendments/create-contract-amendment) |
| [Create Contract Document](actions/create-contract-document.md) | `POST /contracts/:contract_id/documents` | [docs](https://developer.deel.com/api/endpoints/contractor-hiring/create-contract-document) |
| [Create Contract Invitation](actions/create-contract-invitation.md) | `POST /contracts/:contract_id/invitations` | [docs](https://developer.deel.com/api/endpoints/contractor-hiring/create-contract-invitation) |
| [Create Contract Milestone](actions/create-contract-milestone.md) | `POST /contracts/:contract_id/milestones` | [docs](https://developer.deel.com/api/endpoints/milestones/create-contract-milestone) |
| [Create Contract Signature](actions/create-contract-signature.md) | `POST /contracts/:contract_id/signatures` | [docs](https://developer.deel.com/api/endpoints/contractor-hiring/create-contract-signature) |
| [Create Contract Task](actions/create-contract-task.md) | `POST /contracts/:contract_id/tasks` | [docs](https://developer.deel.com/api/endpoints/tasks/create-contract-task) |
| [Create Contract Task Review](actions/create-contract-task-review.md) | `POST /contracts/:contract_id/tasks/:task_id/reviews` | [docs](https://developer.deel.com/api/endpoints/tasks/create-contract-task-review) |
| [Create IC Contract](actions/create-ic-contract.md) | `POST /contracts` | [docs](https://developer.deel.com/api/endpoints/contracts/create-ic-contract) |
| [Create Invoice Adjustment Review](actions/create-invoice-adjustment-review.md) | `POST /invoice-adjustments/:id/reviews` | [docs](https://developer.deel.com/api/endpoints/invoice-adjustments/create-invoice-adjustment-review) |
| [Create Timesheet](actions/create-timesheet.md) | `POST /timesheets` | [docs](https://developer.deel.com/api/endpoints/timesheets/create-timesheet) |
| [Create Timesheet Review](actions/create-timesheet-review.md) | `POST /timesheets/:id/reviews` | [docs](https://developer.deel.com/api/endpoints/timesheets/create-timesheet-review) |
| [Delete Contract Adjustment](actions/delete-contract-adjustment.md) | `DELETE /adjustments/:id` | [docs](https://developer.deel.com/api/endpoints/adjustments/delete-contract-adjustment) |
| [Delete Contract Milestone](actions/delete-contract-milestone.md) | `DELETE /contracts/:contract_id/milestones/:milestone_id` | [docs](https://developer.deel.com/api/endpoints/milestones/delete-contract-milestone) |
| [Delete Contract Task](actions/delete-contract-task.md) | `DELETE /contracts/:contract_id/tasks/:task_id` | [docs](https://developer.deel.com/api/endpoints/tasks/delete-contract-task) |
| [Delete Invoice Adjustment](actions/delete-invoice-adjustment.md) | `DELETE /invoice-adjustments/:id` | [docs](https://developer.deel.com/api/endpoints/invoice-adjustments/delete-invoice-adjustment) |
| [Get Contract](actions/get-contract.md) | `GET /contracts/:contract_id` | [docs](https://developer.deel.com/api/endpoints/contracts/get-contract) |
| [Get Contract Adjustment](actions/get-contract-adjustment.md) | `GET /adjustments/:id` | [docs](https://developer.deel.com/api/endpoints/adjustments/get-contract-adjustment) |
| [Get Contract Invitations](actions/get-contract-invitations.md) | `GET /contracts/:contract_id/invitations` | [docs](https://developer.deel.com/api/endpoints/contractor-hiring/get-contract-invitations) |
| [Get Contract Invite](actions/get-contract-invite.md) | `GET /contracts/:contract_id/invite` | [docs](https://developer.deel.com/api/endpoints/contractor-hiring/get-contract-invite) |
| [Get Contract Milestone by ID](actions/get-contract-milestone-by-id.md) | `GET /contracts/:contract_id/milestones/:milestone_id` | [docs](https://developer.deel.com/api/endpoints/milestones/get-contract-milestone-by-id) |
| [Get Invoice Adjustment by ID](actions/get-invoice-adjustment-by-id.md) | `GET /invoice-adjustments/:id` | [docs](https://developer.deel.com/api/endpoints/invoice-adjustments/get-invoice-adjustment-by-id) |
| [Get Timesheet by ID](actions/get-timesheet-by-id.md) | `GET /timesheets/:id` | [docs](https://developer.deel.com/api/endpoints/timesheets/get-timesheet-by-id) |
| [List Adjustment Categories](actions/list-adjustment-categories.md) | `GET /adjustments/categories` | [docs](https://developer.deel.com/api/endpoints/adjustments/get-adjustment-categories) |
| [List Contract Adjustments](actions/list-contract-adjustments.md) | `GET /contracts/:contract_id/adjustments` | [docs](https://developer.deel.com/api/endpoints/adjustments/get-contract-adjustments) |
| [List Contract Amendments](actions/list-contract-amendments.md) | `GET /contracts/:contract_id/amendments` | [docs](https://developer.deel.com/api/endpoints/contractor-amendments/get-contract-amendments) |
| [List Contract Invoice Adjustments](actions/list-contract-invoice-adjustments.md) | `GET /contracts/:contract_id/invoice-adjustments` | [docs](https://developer.deel.com/api/endpoints/invoice-adjustments/get-contract-invoice-adjustments) |
| [List Contract Milestones](actions/list-contract-milestones.md) | `GET /contracts/:contract_id/milestones` | [docs](https://developer.deel.com/api/endpoints/milestones/get-contract-milestones) |
| [List Contract Payment Cycles](actions/list-contract-payment-cycles.md) | `GET /contracts/:contract_id/payment_cycles` | [docs](https://developer.deel.com/api/endpoints/contractor-hiring/get-contract-payment-cycles) |
| [List Contract Tasks](actions/list-contract-tasks.md) | `GET /contracts/:contract_id/tasks` | [docs](https://developer.deel.com/api/endpoints/tasks/get-contract-tasks) |
| [List Contract Timesheets](actions/list-contract-timesheets.md) | `GET /contracts/:contract_id/timesheets` | [docs](https://developer.deel.com/api/endpoints/timesheets/get-contract-timesheets) |
| [List Contracts](actions/list-contracts.md) | `GET /contracts` | [docs](https://developer.deel.com/api/endpoints/contracts/get-contracts) |
| [List Invoice Adjustments](actions/list-invoice-adjustments.md) | `GET /invoice-adjustments` | [docs](https://developer.deel.com/api/endpoints/invoice-adjustments/get-invoice-adjustments) |
| [List Timesheets](actions/list-timesheets.md) | `GET /timesheets` | [docs](https://developer.deel.com/api/endpoints/timesheets/get-timesheets) |
| [Update Contract Adjustment](actions/update-contract-adjustment.md) | `PATCH /adjustments/:id` | [docs](https://developer.deel.com/api/endpoints/adjustments/update-contract-adjustment) |
| [Update IC Contract](actions/update-ic-contract.md) | `PATCH /contracts/:contract_id` | [docs](https://developer.deel.com/api/endpoints/contracts/update-ic-contract) |
| [Update Timesheet](actions/update-timesheet.md) | `PATCH /timesheets/:id` | [docs](https://developer.deel.com/api/endpoints/timesheets/update-timesheet) |
