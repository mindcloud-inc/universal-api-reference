# <img src="https://images.mindcloud.co/apps/icons/customer-x_1775057612260.png" alt="CustomerX logo" width="28" height="28"> CustomerX: Universal API

Manage customers, contracts, tickets, tasks, and financial records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/customerX/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://customerx.cx/
- **Vendor API docs:** https://doc.api.customerx.com.br/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in CustomerX. |
| [Create Or Update Contact](actions/create-or-update-contact.md) | PUT | Creates or updates a contact in CustomerX. |
| [Delete Contact By External ID](actions/delete-contact-by-external-id.md) | DELETE | Deletes an existing contact from CustomerX by external ID. |
| [Find Contact](actions/find-contact.md) | GET | Finds a contact in CustomerX by search filters. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from CustomerX. |
| [Update Contact By External ID](actions/update-contact-by-external-id.md) | PUT | Updates an existing contact in CustomerX by external ID. |

### Contract Additive

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Additive](actions/create-contract-additive.md) | POST | Creates a new contract additive in CustomerX. |
| [Get Contract Additive](actions/get-contract-additive.md) | GET | Retrieves contract additive details from CustomerX. |
| [List Contract Additives](actions/list-contract-additives.md) | GET | Retrieves a list of contract additives from CustomerX. |
| [Update Contract Additive By External ID](actions/update-contract-additive-by-external-id.md) | PUT | Updates an existing contract additive in CustomerX by external ID. |

### Contract Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Plan](actions/create-contract-plan.md) | POST | Creates a new contract plan in CustomerX. |
| [Get Contract Plan](actions/get-contract-plan.md) | GET | Retrieves contract plan details from CustomerX. |
| [List Contract Plans](actions/list-contract-plans.md) | GET | Retrieves a list of contract plans from CustomerX. |
| [Update Contract Plan By External ID](actions/update-contract-plan-by-external-id.md) | PUT | Updates an existing contract plan in CustomerX by external ID. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Contract](actions/cancel-contract.md) | PUT | Cancels an existing contract in CustomerX. |
| [Create Contract](actions/create-contract.md) | POST | Creates a new contract in CustomerX. |
| [Delete Contract By External ID](actions/delete-contract-by-external-id.md) | DELETE | Deletes an existing contract from CustomerX by external ID. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves a list of contracts from CustomerX. |
| [Reactivate Contract By External ID](actions/reactivate-contract-by-external-id.md) | PUT | Reactivates an existing contract in CustomerX by external ID. |
| [Update Contract By External ID](actions/update-contract-by-external-id.md) | PUT | Updates an existing contract in CustomerX by external ID. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in CustomerX. |
| [Create Or Update Customer](actions/create-or-update-customer.md) | PUT | Creates or updates a customer in CustomerX. |
| [Delete Customer By External ID](actions/delete-customer-by-external-id.md) | DELETE | Deletes an existing customer from CustomerX by external ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from CustomerX. |
| [Reactivate Customer By External ID](actions/reactivate-customer-by-external-id.md) | PUT | Reactivates an existing customer in CustomerX by external ID. |
| [Update Customer By External ID](actions/update-customer-by-external-id.md) | PUT | Updates an existing customer in CustomerX by external ID. |

### Financial

| Action | Method | Description |
| --- | --- | --- |
| [Create Financial](actions/create-financial.md) | POST | Creates a new financial record in CustomerX. |
| [Delete Financial By External ID](actions/delete-financial-by-external-id.md) | DELETE | Deletes an existing financial record from CustomerX by external ID. |
| [List Financials](actions/list-financials.md) | GET | Retrieves a list of financial records from CustomerX. |
| [Update Financial By External ID](actions/update-financial-by-external-id.md) | PUT | Updates an existing financial record in CustomerX by external ID. |

### Journeys

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer Journey](actions/add-customer-journey.md) | POST | Creates a customer journey link in CustomerX. |
| [List Customer Journeys](actions/list-customer-journeys.md) | GET | Retrieves linked customer journeys from CustomerX. |
| [Remove Customer Journey](actions/remove-customer-journey.md) | DELETE | Deletes a customer journey link from CustomerX. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in CustomerX. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from CustomerX. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in CustomerX. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Ticket](actions/create-or-update-ticket.md) | PUT | Creates or updates a ticket in CustomerX. |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in CustomerX. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves a list of tickets from CustomerX. |
| [Update Ticket By External ID](actions/update-ticket-by-external-id.md) | PUT | Updates an existing ticket in CustomerX by external ID. |

