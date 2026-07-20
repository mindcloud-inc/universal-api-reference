# <img src="https://images.mindcloud.co/apps/icons/make-plans-red-web-500x500px-in-box_1778089204390.png" alt="Makeplans logo" width="28" height="28"> Makeplans: Universal API

Scheduling and booking platform for appointments, classes, events, customers, resources, services, coupons, gift cards, orders, and account settings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/makeplans/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://makeplans.com
- **Vendor API docs:** https://developer.makeplans.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Services](actions/list-services.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | PUT | Cancels an existing booking in Makeplans. |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Makeplans. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from Makeplans. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Makeplans. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in Makeplans. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Makeplans. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in Makeplans. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Makeplans. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Makeplans. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in Makeplans. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Makeplans. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Makeplans. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Makeplans. |
| [List People](actions/list-people.md) | GET | Retrieves people from Makeplans. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Makeplans. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Create Resource](actions/create-resource.md) | POST | Creates a new resource in Makeplans. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Makeplans. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from Makeplans. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Makeplans. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a new service in Makeplans. |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from Makeplans. |
| [List Services](actions/list-services.md) | GET | Retrieves services from Makeplans. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing service in Makeplans. |

### Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Service Slots](actions/list-service-slots.md) | GET | Retrieves available service slots from Makeplans. |

