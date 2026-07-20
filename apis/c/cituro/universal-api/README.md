# <img src="https://images.mindcloud.co/apps/icons/cituro-icon-filled-256_1774377237449.png" alt="Cituro logo" width="28" height="28"> Cituro: Universal API

Cituro is a cloud appointment booking and scheduling platform for businesses that manage bookings, customers, ratings, and related workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cituro/latest
- **Category:** Productivity / Scheduling
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cituro.com
- **Vendor API docs:** https://www.cituro.com/help/developers-corner/schnittstellen

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Appointment](actions/get-appointment.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-appointment?connectionId=$CONNECTION_ID&appointmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves an appointment record from Cituro. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves a list of appointments from Cituro. |

### Coupon

| Action | Method | Description |
| --- | --- | --- |
| [Get Coupon](actions/get-coupon.md) | GET | Retrieves a coupon record from Cituro. |
| [List Coupons](actions/list-coupons.md) | GET | Retrieves a list of coupons from Cituro. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer record from Cituro. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Cituro. |
| [Search Customers](actions/search-customers.md) | GET | Finds matching customer records in Cituro. |

### Discount

| Action | Method | Description |
| --- | --- | --- |
| [Get Discount](actions/get-discount.md) | GET | Retrieves a discount record from Cituro. |
| [List Discounts](actions/list-discounts.md) | GET | Retrieves a list of discounts from Cituro. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Location](actions/get-location.md) | GET | Retrieves a location record from Cituro. |
| [List Locations](actions/list-locations.md) | GET | Retrieves a list of locations from Cituro. |

### Rating

| Action | Method | Description |
| --- | --- | --- |
| [List Ratings](actions/list-ratings.md) | GET | Retrieves a list of ratings from Cituro. |

### Rating Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Ratings Summary](actions/get-ratings-summary.md) | GET | Retrieves the ratings summary from Cituro. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource record from Cituro. |
| [List Resources](actions/list-resources.md) | GET | Retrieves a list of resources from Cituro. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET | Retrieves a service record from Cituro. |
| [List Services](actions/list-services.md) | GET | Retrieves a list of services from Cituro. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Cituro. |

