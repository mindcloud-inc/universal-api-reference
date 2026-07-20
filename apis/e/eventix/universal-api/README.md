# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-20-as-16_1776712753084.png" alt="Eventix logo" width="28" height="28"> Eventix: Universal API

Eventix is an event ticketing platform for managing events, shops, tickets, products, orders, coupons, and related reporting through the Weeztix API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eventix/latest
- **Category:** Support / Ticketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eventix.io
- **Vendor API docs:** https://docs.weeztix.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Events](actions/get-events.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-events?connectionId=$CONNECTION_ID&type=normal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific Coupon](actions/get-coupon-specific.md) | GET | Retrieves a specific coupon from Eventix. |
| [Get Coupons](actions/get-coupons.md) | GET | Retrieves coupons from Eventix. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific EventDate](actions/get-event-date-specific.md) | GET | Retrieves a specific event date from Eventix. |
| [Retrieve the Event of an EventDate](actions/get-event-date-specific-event.md) | GET | Retrieves the parent event of an Eventix event date. |
| [Retrieve the Location of an EventDate](actions/get-event-date-specific-location.md) | GET | Retrieves the location of an Eventix event date. |
| [Get EventDates](actions/get-event-dates.md) | GET | Retrieves event dates from Eventix. |
| [Get a specific Event](actions/get-event-specific.md) | GET | Retrieves a specific event from Eventix. |
| [Get analysis of an Event](actions/get-event-specific-analysis.md) | GET | Retrieves analysis for an Eventix event. |
| [Get EventDates for Event](actions/get-event-specific-event-dates.md) | GET | Retrieves event dates for an Eventix event. |
| [Get EventDates for Event with Products](actions/get-event-specific-event-dates-with-products.md) | GET | Retrieves event dates with products for an Eventix event. |
| [Get Location of Event](actions/get-event-specific-event-location.md) | GET | Retrieves the location of an Eventix event. |
| [Get Scanning stats for an event](actions/get-event-specific-scanning-stats.md) | GET | Retrieves scanning stats for an Eventix event. |
| [Get all Shops of an Event](actions/get-event-specific-shops.md) | GET | Retrieves shops for an Eventix event. |
| [Get Ticket Types for Event](actions/get-event-tickets.md) | GET | Retrieves ticket types for an Eventix event. |
| [Get Ticket Types for Event with Products](actions/get-event-tickets-with-products.md) | GET | Retrieves ticket types with products for an Eventix event. |
| [Get Ticket Types for Event with Shops](actions/get-event-tickets-with-shops.md) | GET | Retrieves ticket types with shops for an Eventix event. |
| [Get Events](actions/get-events.md) | GET | Retrieves events from Eventix. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a specific Location](actions/get-event-location-specific.md) | GET | Retrieves a specific location from Eventix. |
| [Get EventDates for specific Location](actions/get-event-location-specific-event-dates.md) | GET | Retrieves event dates for an Eventix location. |
| [Get Locations](actions/get-event-locations.md) | GET | Retrieves locations from Eventix. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get an entire specific Order](actions/get-order-specific.md) | GET | Retrieves a specific order from Eventix. |
| [Get Order status link](actions/search-order-by-payment-id.md) | GET | Finds an Eventix order status link by payment ID. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get specific Product Type](actions/get-product-specific.md) | GET | Retrieves a specific product type from Eventix. |
| [Get attached EventDates of Product Type](actions/get-product-specific-event-dates.md) | GET | Retrieves event dates for an Eventix product type. |
| [Get attached Metadata of Product Type](actions/get-product-specific-metadata.md) | GET | Retrieves metadata for an Eventix product type. |
| [Get Ticket Types of Product Type](actions/get-product-specific-tickets.md) | GET | Retrieves ticket types for an Eventix product type. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific Ticket Type](actions/get-ticket-specific.md) | GET | Retrieves a specific ticket type from Eventix. |
| [Get attached EventDates of Ticket Type](actions/get-ticket-specific-event-dates.md) | GET | Retrieves event dates for an Eventix ticket type. |
| [Get all ProductGroups for this Ticket Type](actions/get-ticket-specific-product-groups.md) | GET | Retrieves product groups for an Eventix ticket type. |
| [Get all ProductGroups with Product Types for this Ticket Type](actions/get-ticket-specific-product-groups-with-products.md) | GET | Retrieves product groups with products for an Eventix ticket type. |
| [Retrieve all Product Types attached to this Ticket Type](actions/get-ticket-specific-products.md) | GET | Retrieves product types for an Eventix ticket type. |
| [Get all Shops this Ticket Type is attached to](actions/ticket-list-shops.md) | GET | Retrieves shops for an Eventix ticket type. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get a specific Shop](actions/get-shop-specific.md) | GET | Retrieves a specific shop from Eventix. |
| [Get attached Metadata of Shop](actions/get-shop-specific-metadata.md) | GET | Retrieves metadata for an Eventix shop. |
| [Get a specific Shop's options](actions/get-shop-specific-options.md) | GET | Retrieves options for an Eventix shop. |
| [Get attached PaymentMethods of Shop](actions/get-shop-specific-payment-methods.md) | GET | Retrieves payment methods for an Eventix shop. |
| [Get attached Products of Shop](actions/get-shop-specific-product.md) | GET | Retrieves products for an Eventix shop. |
| [Get attached ShopTrackers of Shop](actions/get-shop-specific-shop-trackers.md) | GET | Retrieves shop trackers for an Eventix shop. |
| [Get attached Ticket Types of Shop](actions/get-shop-specific-ticket.md) | GET | Retrieves ticket types for an Eventix shop. |
| [Get Shops](actions/get-shops.md) | GET | Retrieves shops from Eventix. |

