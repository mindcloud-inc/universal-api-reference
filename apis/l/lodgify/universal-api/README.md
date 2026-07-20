# <img src="https://images.mindcloud.co/apps/icons/lodgify_1773411423046.png" alt="Lodgify logo" width="28" height="28"> Lodgify: Universal API

Manage Lodgify properties, availability, reservations, rates, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lodgify/latest
- **Category:** Commerce
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lodgify.com
- **Vendor API docs:** https://docs.lodgify.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Properties](actions/list-properties.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [List Availability](actions/list-availability.md) | GET | Retrieves availability calendar data from Lodgify. |
| [Update Room Availability](actions/update-room-availability.md) | PUT | Updates a room's availability in Lodgify. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves a list of countries from Lodgify. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves a list of currencies from Lodgify. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Property](actions/get-property.md) | GET | Retrieves details for a property from Lodgify. |
| [List Properties](actions/list-properties.md) | GET | Retrieves a list of properties from Lodgify. |

### Rate Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate Calendar](actions/get-rate-calendar.md) | GET | Retrieves a nightly rate calendar from Lodgify. |

### Reservation

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | GET | Retrieves details for a booking from Lodgify. |
| [Get Thread Details](actions/get-thread-details.md) | GET | Retrieves message thread details from Lodgify. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings and enquiries from Lodgify. |
| [Update Reservation Status](actions/update-reservation-status.md) | PUT | Updates a booking's status in Lodgify. |

### Room

| Action | Method | Description |
| --- | --- | --- |
| [List Available Rooms](actions/list-available-rooms.md) | GET | Retrieves available room types from Lodgify. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from Lodgify. |

