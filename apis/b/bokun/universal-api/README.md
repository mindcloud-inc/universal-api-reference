# <img src="https://images.mindcloud.co/apps/icons/bokun_1774536652737.png" alt="Bokun logo" width="28" height="28"> Bokun: Universal API

Bokun signed REST API integration using Bokun access key and secret key authentication for official REST endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bokun/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bokun.io
- **Vendor API docs:** https://api-docs.bokun.dev/rest-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Time Zones](actions/list-time-zones.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-time-zones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Availability

| Action | Method | Description |
| --- | --- | --- |
| [List Experience Availability](actions/list-experience-availability.md) | GET | Retrieves availability for an experience product from Bokun. |
| [List Experience Availability Statistics](actions/list-experience-availability-statistics.md) | GET | Retrieves availability statistics for an experience product from Bokun. |
| [List Experience Closeouts](actions/list-experience-closeouts.md) | GET | Retrieves availability closeouts for an experience product from Bokun. |

### Bookings

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Audit Trail](actions/get-booking-audit-trail.md) | GET | Retrieves audit trail records for a booking from Bokun. |
| [Get Booking Payments](actions/get-booking-payments.md) | GET | Retrieves customer payments for a booking from Bokun. |
| [List Experience Booking Notes](actions/list-experience-booking-notes.md) | GET | Retrieves notes for an experience booking from Bokun. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer by ID from Bokun. |

### Experiences

| Action | Method | Description |
| --- | --- | --- |
| [List Experience IDs](actions/list-experience-ids.md) | GET | Retrieves owned experience product IDs from Bokun. |

### General

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves supported country records from Bokun. |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves supported time zones from Bokun. |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Price Schedule](actions/get-price-schedule.md) | GET | Retrieves a price schedule by ID from Bokun. |
| [Get Pricing Category](actions/get-pricing-category.md) | GET | Retrieves a pricing category by ID from Bokun. |
| [Get Promo Code](actions/get-promo-code.md) | GET | Retrieves a promo code by ID from Bokun. |
| [Get Tax](actions/get-tax.md) | GET | Retrieves a tax by ID from Bokun. |
| [List Cancellation Policies](actions/list-cancellation-policies.md) | GET | Retrieves cancellation policies from the current Bokun vendor. |
| [List Price Catalogs](actions/list-price-catalogs.md) | GET | Retrieves price catalogs owned by the current Bokun vendor. |
| [List Price Schedules](actions/list-price-schedules.md) | GET | Retrieves price schedules from the current Bokun vendor. |
| [List Pricing Categories](actions/list-pricing-categories.md) | GET | Retrieves pricing categories from the current Bokun vendor. |
| [List Promo Codes](actions/list-promo-codes.md) | GET | Retrieves promo codes from the current Bokun vendor. |
| [List Taxes](actions/list-taxes.md) | GET | Retrieves taxes owned by the current Bokun vendor. |

### Resources

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource by ID from Bokun. |
| [Get Resource Pool](actions/get-resource-pool.md) | GET | Retrieves a resource pool by ID from Bokun. |
| [List Resource Pools](actions/list-resource-pools.md) | GET | Retrieves resource pool records from Bokun. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources and capacity details from Bokun. |

