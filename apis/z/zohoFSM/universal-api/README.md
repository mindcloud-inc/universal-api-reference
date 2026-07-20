# <img src="https://images.mindcloud.co/apps/icons/zoho-fsm_1773941020296.png" alt="Zoho FSM logo" width="28" height="28"> Zoho FSM: Universal API

Zoho FSM helps teams manage field service requests, work orders, appointments, contacts, companies, and estimates through Zoho's field service API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoFSM/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/fsm/
- **Vendor API docs:** https://www.zoho.com/fsm/developer/help/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Requests](actions/list-requests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a new company in Zoho FSM. |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from Zoho FSM. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Zoho FSM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Zoho FSM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves contact details from Zoho FSM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Zoho FSM. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in Zoho FSM. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves estimate details from Zoho FSM. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from Zoho FSM. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Request](actions/create-request.md) | POST | Creates a new request in Zoho FSM. |
| [Get Request](actions/get-request.md) | GET | Retrieves request details from Zoho FSM. |
| [List Requests](actions/list-requests.md) | GET | Retrieves requests from Zoho FSM. |
| [Update Request](actions/update-request.md) | PUT | Updates an existing request in Zoho FSM. |

### Request Transition

| Action | Method | Description |
| --- | --- | --- |
| [List Request Transitions](actions/list-request-transitions.md) | GET | Retrieves available request transitions from Zoho FSM. |
| [Perform Request Transition](actions/perform-request-transition.md) | PUT | Performs a request blueprint transition in Zoho FSM. |

### Service Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Appointment](actions/create-service-appointment.md) | POST | Creates a new service appointment in Zoho FSM. |
| [List Service Appointments](actions/list-service-appointments.md) | GET | Retrieves service appointments from Zoho FSM. |
| [Update Service Appointment](actions/update-service-appointment.md) | PUT | Updates an existing service appointment in Zoho FSM. |

### Work Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Work Order](actions/create-work-order.md) | POST | Creates a new work order in Zoho FSM. |
| [Get Work Order](actions/get-work-order.md) | GET | Retrieves work order details from Zoho FSM. |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves work orders from Zoho FSM. |
| [Update Work Order](actions/update-work-order.md) | PUT | Updates an existing work order in Zoho FSM. |

### Work Order Transition

| Action | Method | Description |
| --- | --- | --- |
| [List Work Order Transitions](actions/list-work-order-transitions.md) | GET | Retrieves available work order transitions from Zoho FSM. |
| [Perform Work Order Transition](actions/perform-work-order-transition.md) | PUT | Performs a work order blueprint transition in Zoho FSM. |

