# <img src="https://images.mindcloud.co/apps/icons/rem-online_1776877930031.png" alt="RemOnline logo" width="28" height="28"> RemOnline: Universal API

Manage jobs, clients, inventory, scheduling, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remOnline/latest
- **Category:** Support / Field Service
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://roapp.io/
- **Vendor API docs:** https://roapp.readme.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Settings](actions/get-company-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves a list of bookings from RemOnline. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Information](actions/get-company-information.md) | GET | Retrieves your company information from RemOnline. |

### Company Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Settings](actions/get-company-settings.md) | GET | Retrieves your company settings from RemOnline. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves a list of estimates from RemOnline. |

### Estimate Status

| Action | Method | Description |
| --- | --- | --- |
| [List Estimate Statuses](actions/list-estimate-statuses.md) | GET | Retrieves a list of estimate statuses from RemOnline. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from RemOnline. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from RemOnline. |

### Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Order Statuses](actions/list-order-statuses.md) | GET | Retrieves a list of order statuses from RemOnline. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST | Creates a new organization in RemOnline. |
| [Get Organization By ID](actions/get-organization-by-id.md) | GET | Retrieves an organization from RemOnline by ID. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from RemOnline. |
| [Update Organization](actions/update-organization.md) | PUT | Updates an existing organization in RemOnline. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in RemOnline. |
| [Get Person By ID](actions/get-person-by-id.md) | GET | Retrieves a person from RemOnline by ID. |
| [List People](actions/list-people.md) | GET | Retrieves a list of people from RemOnline. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in RemOnline. |

