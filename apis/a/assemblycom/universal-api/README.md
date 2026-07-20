# <img src="https://images.mindcloud.co/apps/icons/idd0iz-pu1f-1773776828251_1773776835773.png" alt="Assembly.com logo" width="28" height="28"> Assembly.com: Universal API

Manage clients, tasks, contracts, invoices, and messages

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/assemblycom/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.assembly.com
- **Vendor API docs:** https://docs.assembly.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List App Installs](actions/list-app-installs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-app-installs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### App Install

| Action | Method | Description |
| --- | --- | --- |
| [List App Installs](actions/list-app-installs.md) | GET | Retrieves app installs in the current Assembly.com workspace. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Assembly.com. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Assembly.com. |
| [Retrieve Client](actions/retrieve-client.md) | GET | Retrieves a client from Assembly.com by ID. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Assembly.com. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Assembly.com. |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves a company from Assembly.com by ID. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Assembly.com. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from Assembly.com. |
| [Retrieve Contract](actions/retrieve-contract.md) | GET | Retrieves a contract from Assembly.com by ID. |
| [Send Contract](actions/send-contract.md) | POST | Sends a contract in Assembly.com. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates an invoice in Assembly.com. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Assembly.com. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves an invoice from Assembly.com by ID. |

### Message Channel

| Action | Method | Description |
| --- | --- | --- |
| [Create Message Channel](actions/create-message-channel.md) | POST | Creates a message channel in Assembly.com. |
| [List Message Channels](actions/list-message-channels.md) | GET | Retrieves message channels from Assembly.com. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from an Assembly.com message channel. |
| [Send Message](actions/send-message.md) | POST | Sends a message in an Assembly.com message channel. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a note in Assembly.com. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Assembly.com. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Assembly.com. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels an existing subscription in Assembly.com. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in Assembly.com. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Assembly.com. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Assembly.com. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Assembly.com. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from Assembly.com by ID. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Assembly.com. |

