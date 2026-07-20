# <img src="https://images.mindcloud.co/apps/icons/bookingmood_1774292262029.png" alt="Bookingmood logo" width="28" height="28"> Bookingmood: Universal API

Manage bookings, calendars, guests, payments, and rental websites

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bookingmood/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bookingmood.com
- **Vendor API docs:** https://www.bookingmood.com/en-US/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [Query Availability](actions/query-availability.md) | GET | Retrieves long-range availability for multiple Bookingmood products. |
| [Search Availability](actions/search-availability.md) | GET | Finds Bookingmood product availability by interval, occupancy, and attribute options. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Book](actions/book.md) | POST | Creates a booking in Bookingmood from product, interval, occupancy, and form values. |
| [Delete Bookings](actions/delete-bookings.md) | DELETE | Deletes booking records from the Bookingmood API. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves booking records from the Bookingmood API. |
| [Update Bookings](actions/update-bookings.md) | PUT | Updates booking records in the Bookingmood API. |

### Calendar Event

| Action | Method | Description |
| --- | --- | --- |
| [Delete Calendar Events](actions/delete-calendar-events.md) | DELETE | Deletes calendar event records from the Bookingmood API. |
| [List Calendar Events](actions/list-calendar-events.md) | GET | Retrieves calendar event records from the Bookingmood API. |
| [Update Calendar Events](actions/update-calendar-events.md) | PUT | Updates calendar event records in the Bookingmood API. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in the Bookingmood API. |
| [Delete Contacts](actions/delete-contacts.md) | DELETE | Deletes contact records from the Bookingmood API. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from the Bookingmood API. |
| [Update Contacts](actions/update-contacts.md) | PUT | Updates contact records in the Bookingmood API. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in the Bookingmood API. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoice records from the Bookingmood API. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages scheduled or sent to Bookingmood guests. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in the Bookingmood API. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payment records from the Bookingmood API. |
| [Update Payments](actions/update-payments.md) | PUT | Updates payment records in the Bookingmood API. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in the Bookingmood API. |
| [Delete Products](actions/delete-products.md) | DELETE | Deletes product records from the Bookingmood API. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from the Bookingmood API. |
| [Update Products](actions/update-products.md) | PUT | Updates product records in the Bookingmood API. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [List Sites](actions/list-sites.md) | GET | Retrieves site records from the Bookingmood API. |

