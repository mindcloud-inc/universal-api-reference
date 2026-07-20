# <img src="https://images.mindcloud.co/apps/icons/bookafy_1774022405091.png" alt="Bookafy logo" width="28" height="28"> Bookafy: Universal API

Schedule appointments, manage customers, and coordinate staff availability

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bookafy/latest
- **Category:** Productivity / Scheduling
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bookafy.com/
- **Vendor API docs:** https://app.bookafy.com/api-docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Staff Users](actions/list-staff-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-staff-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Api Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves webhook subscriptions from Bookafy. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates an appointment in Bookafy. |
| [Delete Appointment](actions/delete-appointment.md) | DELETE | Deletes or cancels an appointment in Bookafy. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves appointments from Bookafy by date range. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an appointment in Bookafy. |

### Appointment Type

| Action | Method | Description |
| --- | --- | --- |
| [List Appointment Types with Booking Links](actions/list-appointment-types-with-booking-links.md) | GET | Retrieves appointment types and booking links from Bookafy. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Bookafy. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes a customer from Bookafy. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Bookafy. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Bookafy. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in Bookafy. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [List Staff Users](actions/list-staff-users.md) | GET | Retrieves staff users from Bookafy. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Services with Details](actions/list-services-with-details.md) | GET | Retrieves services with details from Bookafy. |

