# <img src="https://images.mindcloud.co/apps/icons/pretix_1776783345760.png" alt="pretix logo" width="28" height="28"> pretix: Universal API

pretix is an open-source and hosted ticketing platform for selling tickets, managing events, orders, vouchers, check-in workflows, teams, and event operations through a documented REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pretix/latest
- **Category:** Support / Ticketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pretix.eu/
- **Vendor API docs:** https://docs.pretix.eu/dev/api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Get Voucher](actions/get-voucher.md) | GET | Retrieves a voucher from pretix. |
| [List Vouchers](actions/list-vouchers.md) | GET | Retrieves vouchers from a pretix event. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from pretix. |
| [Get Event Settings](actions/get-event-settings.md) | GET | Retrieves event settings from pretix. |
| [Get Sub Event](actions/get-sub-event.md) | GET | Retrieves a sub-event from pretix. |
| [List Events](actions/list-events.md) | GET | Retrieves events from a pretix organizer. |
| [List Sub Events](actions/list-sub-events.md) | GET | Retrieves sub-events from a pretix event. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download Invoice](actions/download-invoice.md) | GET | Retrieves an invoice download from pretix. |
| [Download Order Ticket PDF](actions/download-order-ticket-pdf.md) | GET | Retrieves an order ticket PDF from pretix. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [Get Quota](actions/get-quota.md) | GET | Retrieves a quota from pretix. |
| [Get Quota Availability](actions/get-quota-availability.md) | GET | Retrieves quota availability from pretix. |
| [List Quotas](actions/list-quotas.md) | GET | Retrieves quotas from a pretix event. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from pretix. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from a pretix event. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get Check In List](actions/get-check-in-list.md) | GET | Retrieves a check-in list from pretix. |
| [List Check In Lists](actions/list-check-in-lists.md) | GET | Retrieves check-in lists from a pretix event. |

### Order Lines

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Position](actions/get-order-position.md) | GET | Retrieves an order position from pretix. |
| [List Order Positions](actions/list-order-positions.md) | GET | Retrieves order positions from a pretix event. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from pretix. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from a pretix event. |
| [Search Organizer Orders](actions/search-organizer-orders.md) | GET | Searches orders across a pretix organizer. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organizer](actions/get-organizer.md) | GET | Retrieves an organizer from pretix. |
| [Get Organizer Settings](actions/get-organizer-settings.md) | GET | Retrieves organizer settings from pretix. |
| [List Organizers](actions/list-organizers.md) | GET | Retrieves organizers from pretix. |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Variation](actions/get-item-variation.md) | GET | Retrieves an item variation from pretix. |
| [List Item Variations](actions/list-item-variations.md) | GET | Retrieves item variations from pretix. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from pretix. |
| [List Items](actions/list-items.md) | GET | Retrieves items from a pretix event. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Search Check In Tickets](actions/search-check-in-tickets.md) | GET | Searches check-in tickets in pretix. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves your pretix user profile. |

