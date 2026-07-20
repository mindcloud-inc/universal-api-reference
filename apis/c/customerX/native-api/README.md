# CustomerX: Native API Reference

A consolidated summary of CustomerX's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://doc.api.customerx.com.br/
- **API base URL:** `https://sandbox.api.customerx.com.br`

## Authentication

### API Key

Authenticate CustomerX requests with the user API token sent in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://doc.api.customerx.com.br/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer Journey](actions/add-customer-journey.md) | `POST /api/v1/clients/journeys_clients` | [docs](https://doc.api.customerx.com.br/?version=latest#c2eef5dc-a3a4-4398-b513-5857368f117d) |
| [Cancel Contract](actions/cancel-contract.md) | `POST /api/v1/cancel_contracts` | [docs](https://doc.api.customerx.com.br/?version=latest#52aade67-7950-4e6e-b824-afbca2ede9e1) |
| [Create Contact](actions/create-contact.md) | `POST /api/v1/contacts` | [docs](https://doc.api.customerx.com.br/?version=latest#ba01accb-8fef-4499-999d-13b0520fdaad) |
| [Create Contract](actions/create-contract.md) | `POST /api/v1/contracts` | [docs](https://doc.api.customerx.com.br/?version=latest#2fc28bcd-97a4-429f-8079-f70e7854031a) |
| [Create Contract Additive](actions/create-contract-additive.md) | `POST /api/v1/contract_additives` | [docs](https://doc.api.customerx.com.br/?version=latest#c6d28cfd-1162-4719-b5db-ff32800a8737) |
| [Create Contract Plan](actions/create-contract-plan.md) | `POST /api/v1/contract_plans` | [docs](https://doc.api.customerx.com.br/?version=latest#3161c013-fdb2-4954-b7cb-e5b2e20ee24d) |
| [Create Customer](actions/create-customer.md) | `POST /api/v1/clients` | [docs](https://doc.api.customerx.com.br/?version=latest#75ce15f7-1214-46e3-bf5b-f12f07f4ed7f) |
| [Create Financial](actions/create-financial.md) | `POST /api/v1/financials` | [docs](https://doc.api.customerx.com.br/?version=latest#8fa1b02a-69f7-4957-a498-50c33bec567e) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /api/v1/contacts/create_or_update` | [docs](https://doc.api.customerx.com.br/?version=latest#79f51667-25ec-4b21-947b-b01e21594cd8) |
| [Create Or Update Customer](actions/create-or-update-customer.md) | `POST /api/v1/clients/create_or_update` | [docs](https://doc.api.customerx.com.br/?version=latest#88a2b895-968c-4854-9506-1a421278d99b) |
| [Create Or Update Ticket](actions/create-or-update-ticket.md) | `POST /api/v1/tickets/create_or_update` | [docs](https://doc.api.customerx.com.br/?version=latest#a310538c-c0a0-42ac-af8e-44e2b62451af) |
| [Create Task](actions/create-task.md) | `POST /api/v1/tasks` | [docs](https://doc.api.customerx.com.br/?version=latest#778e2927-b80f-4cf7-960e-0bf7abe4557d) |
| [Create Ticket](actions/create-ticket.md) | `POST /api/v1/tickets` | [docs](https://doc.api.customerx.com.br/?version=latest#5feeb028-28d0-437e-955c-3e42f34e47e4) |
| [Delete Contact By External ID](actions/delete-contact-by-external-id.md) | `DELETE /api/v1/contacts` | [docs](https://doc.api.customerx.com.br/?version=latest#73e29b9f-7240-400c-b40d-6d7c7099a899) |
| [Delete Contract By External ID](actions/delete-contract-by-external-id.md) | `DELETE /api/v1/contracts` | [docs](https://doc.api.customerx.com.br/?version=latest#15a58fe7-b5cb-4c24-a058-f92900f19ff9) |
| [Delete Customer By External ID](actions/delete-customer-by-external-id.md) | `DELETE /api/v1/clients` | [docs](https://doc.api.customerx.com.br/?version=latest#1fb8307a-3885-4476-8459-acfaa77cb877) |
| [Delete Financial By External ID](actions/delete-financial-by-external-id.md) | `DELETE /api/v1/financials` | [docs](https://doc.api.customerx.com.br/?version=latest#1f6a86d4-1e22-42bb-8fc3-728609c30154) |
| [Find Contact](actions/find-contact.md) | `GET /api/v1/contacts/find` | [docs](https://doc.api.customerx.com.br/?version=latest#3f4634f8-faaf-4319-b397-1673585fc66b) |
| [Get Contract Additive](actions/get-contract-additive.md) | `GET /api/v1/contract_additives/[:id]` | [docs](https://doc.api.customerx.com.br/?version=latest#546e6c53-6d11-418c-8df5-ceb79e66ca45) |
| [Get Contract Plan](actions/get-contract-plan.md) | `GET /api/v1/contract_plans/[:id]` | [docs](https://doc.api.customerx.com.br/?version=latest#48a2d107-7190-4c6a-b4ec-e8715b7ba459) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v1/contacts` | [docs](https://doc.api.customerx.com.br/?version=latest#c6dddf3e-13a3-4d2d-bd0d-81c1bdf1a5c3) |
| [List Contract Additives](actions/list-contract-additives.md) | `GET /api/v1/contract_additives` | [docs](https://doc.api.customerx.com.br/?version=latest#10315419-0e90-4955-af33-7a7fe3fe149a) |
| [List Contract Plans](actions/list-contract-plans.md) | `GET /api/v1/contract_plans` | [docs](https://doc.api.customerx.com.br/?version=latest#42dcf0e4-b950-4bb4-a2d1-164944455693) |
| [List Contracts](actions/list-contracts.md) | `GET /api/v1/contracts` | [docs](https://doc.api.customerx.com.br/?version=latest#1d520661-8731-49c8-bd9b-9a22d6859461) |
| [List Customer Journeys](actions/list-customer-journeys.md) | `GET /api/v1/clients/journeys_clients` | [docs](https://doc.api.customerx.com.br/?version=latest#13c6f240-c8d5-4e92-b3fb-bfebbcaf5b8e) |
| [List Customers](actions/list-customers.md) | `GET /api/v1/clients` | [docs](https://doc.api.customerx.com.br/?version=latest#276f1af5-fadd-4b44-82b5-236af1738c8c) |
| [List Financials](actions/list-financials.md) | `GET /api/v1/financials` | [docs](https://doc.api.customerx.com.br/?version=latest#9003e023-03af-4ea5-92b9-11906313e48e) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v1/tasks` | [docs](https://doc.api.customerx.com.br/?version=latest#aae07b23-f390-4040-9df4-7ad0a0ff09bf) |
| [List Tickets](actions/list-tickets.md) | `GET /api/v1/tickets` | [docs](https://doc.api.customerx.com.br/?version=latest#2833a454-fb40-46b7-9e11-4a780af88e02) |
| [Reactivate Contract By External ID](actions/reactivate-contract-by-external-id.md) | `POST /api/v1/contracts/reactivate_contract` | [docs](https://doc.api.customerx.com.br/?version=latest#95e39292-3eb1-42a1-8a59-0271ff6e19c8) |
| [Reactivate Customer By External ID](actions/reactivate-customer-by-external-id.md) | `PUT /api/v1/clients/[:external_id_client]/reactivate` | [docs](https://doc.api.customerx.com.br/?version=latest#4a4dc59a-848b-4888-82f4-c914362ea427) |
| [Remove Customer Journey](actions/remove-customer-journey.md) | `DELETE /api/v1/clients/journeys_clients` | [docs](https://doc.api.customerx.com.br/?version=latest#a330d335-df86-4b8e-aa1c-c502f45c8b86) |
| [Update Contact By External ID](actions/update-contact-by-external-id.md) | `PUT /api/v1/contacts` | [docs](https://doc.api.customerx.com.br/?version=latest#2d21e78d-d34b-46c4-be5c-7e9b9d556ad1) |
| [Update Contract Additive By External ID](actions/update-contract-additive-by-external-id.md) | `PUT /api/v1/contract_additives` | [docs](https://doc.api.customerx.com.br/?version=latest#52561a54-9340-4d7e-8218-fc76b10c5895) |
| [Update Contract By External ID](actions/update-contract-by-external-id.md) | `PUT /api/v1/contracts` | [docs](https://doc.api.customerx.com.br/?version=latest#5c518577-8c42-4e40-8475-09ae7a0f0888) |
| [Update Contract Plan By External ID](actions/update-contract-plan-by-external-id.md) | `PUT /api/v1/contract_plans` | [docs](https://doc.api.customerx.com.br/?version=latest#db3db56d-5716-408c-8885-fadd34380117) |
| [Update Customer By External ID](actions/update-customer-by-external-id.md) | `PUT /api/v1/clients` | [docs](https://doc.api.customerx.com.br/?version=latest#1251a72c-b705-427a-8fe9-def1fdb96cab) |
| [Update Financial By External ID](actions/update-financial-by-external-id.md) | `PUT /api/v1/financials` | [docs](https://doc.api.customerx.com.br/?version=latest#eb0b3d64-4889-486d-87a9-929db6894e95) |
| [Update Task](actions/update-task.md) | `PUT /api/v1/tasks/[:id]` | [docs](https://doc.api.customerx.com.br/?version=latest#cd91ab7e-b37b-4348-8041-93b9ea600352) |
| [Update Ticket By External ID](actions/update-ticket-by-external-id.md) | `PUT /api/v1/tickets` | [docs](https://doc.api.customerx.com.br/?version=latest#3d4d2e08-5f56-444d-ab3d-0da076b32b98) |
