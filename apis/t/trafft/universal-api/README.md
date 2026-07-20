# <img src="https://images.mindcloud.co/apps/icons/trafft_1773850830952.png" alt="Trafft logo" width="28" height="28"> Trafft: Universal API

Manage Trafft bookings, customers, services, and staff

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/trafft/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://trafft.com/
- **Vendor API docs:** https://documenter.getpostman.com/view/1487056/2sAY4x9MRe

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from Trafft. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Trafft. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Trafft. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Trafft. |
| [Get Customer by ID](actions/get-customer-by-id.md) | GET | Retrieves a customer from Trafft by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Trafft. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Trafft. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from Trafft. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Trafft. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET | Retrieves services from Trafft. |

