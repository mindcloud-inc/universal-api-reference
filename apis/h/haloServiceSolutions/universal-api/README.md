# <img src="https://images.mindcloud.co/apps/icons/halo-service-solutions_1773952976672.png" alt="Halo Service Solutions logo" width="28" height="28"> Halo Service Solutions: Universal API

Manage Halo tickets, customers, sites, and users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/haloServiceSolutions/latest
- **Category:** Support / Ticketing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://usehalo.com/halopsa
- **Vendor API docs:** https://usehalo.com/swagger/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Agent](actions/get-current-agent.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-current-agent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Create Action](actions/create-action.md) | POST | Creates a new action in Halo Service Solutions. |
| [Get Action](actions/get-action.md) | GET | Retrieves an action from Halo Service Solutions. |
| [List Actions](actions/list-actions.md) | GET | Retrieves actions from Halo Service Solutions. |

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in Halo Service Solutions. |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves an appointment from Halo Service Solutions. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from Halo Service Solutions. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | POST | Creates a new asset in Halo Service Solutions. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from Halo Service Solutions. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from Halo Service Solutions. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Halo Service Solutions. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Halo Service Solutions. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Halo Service Solutions. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Halo Service Solutions. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Halo Service Solutions. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Halo Service Solutions. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in Halo Service Solutions. |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Halo Service Solutions. |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from Halo Service Solutions. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Halo Service Solutions. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Halo Service Solutions. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Halo Service Solutions. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST | Creates a new purchase order in Halo Service Solutions. |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from Halo Service Solutions. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from Halo Service Solutions. |

### Request For Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Quotation](actions/create-quotation.md) | POST | Creates a new quotation in Halo Service Solutions. |
| [Get Quotation](actions/get-quotation.md) | GET | Retrieves a quotation from Halo Service Solutions. |
| [List Quotations](actions/list-quotations.md) | GET | Retrieves quotations from Halo Service Solutions. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Order](actions/create-sales-order.md) | POST | Creates a new sales order in Halo Service Solutions. |
| [Get Sales Order](actions/get-sales-order.md) | GET | Retrieves a sales order from Halo Service Solutions. |
| [List Sales Orders](actions/list-sales-orders.md) | GET | Retrieves sales orders from Halo Service Solutions. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST | Creates a new ticket in Halo Service Solutions. |
| [Get Ticket](actions/get-ticket.md) | GET | Retrieves a ticket from Halo Service Solutions. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from Halo Service Solutions. |
| [View Tickets](actions/view-tickets.md) | GET | Retrieves tickets from a Halo Service Solutions ticket view. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | POST | Creates a new agent in Halo Service Solutions. |
| [Create User](actions/create-user.md) | POST | Creates a new user in Halo Service Solutions. |
| [Get Agent](actions/get-agent.md) | GET | Retrieves an agent from Halo Service Solutions. |
| [Get Current Agent](actions/get-current-agent.md) | GET | Retrieves the current agent from Halo Service Solutions. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Halo Service Solutions. |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents from Halo Service Solutions. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Halo Service Solutions. |

