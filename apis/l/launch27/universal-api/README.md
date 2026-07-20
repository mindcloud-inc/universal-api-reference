# <img src="https://images.mindcloud.co/apps/icons/launch27_1773680235668.png" alt="Launch27 logo" width="28" height="28"> Launch27: Universal API

Manage bookings, quotes, services, and customer scheduling

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/launch27/latest
- **Category:** Productivity / Scheduling
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.launch27.com/
- **Vendor API docs:** https://api.launch27.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get General Settings](actions/get-general-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-general-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Billing Authorization

| Action | Method | Description |
| --- | --- | --- |
| [Authorize Billing Charge](actions/authorize-billing-charge.md) | PUT | Authorizes a billing charge in Launch27. |

### Billing Setup Intent

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Setup Intent](actions/get-billing-setup-intent.md) | GET | Retrieves a billing setup intent from Launch27. |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Launch27. |

### Booking Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Booking Price](actions/estimate-booking-price.md) | GET | Retrieves a booking price estimate from Launch27. |

### Booking Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Form](actions/get-booking-form.md) | GET | Retrieves a booking form from Launch27. |

### Booking Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking Quote](actions/get-booking-quote.md) | GET | Retrieves a booking quote from Launch27. |

### Booking Spot Day

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Spots](actions/list-booking-spots.md) | GET | Retrieves available booking spots from Launch27. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Custom Fields](actions/list-booking-custom-fields.md) | GET | Retrieves booking custom fields from Launch27. |

### Frequency

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Frequencies](actions/list-booking-frequencies.md) | GET | Retrieves booking frequencies from Launch27. |

### Fspay Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Exchange FSPay Payment Account](actions/exchange-fspay-payment-account.md) | PUT | Exchanges an FSPay payment account in Launch27. |

### Fspay Token

| Action | Method | Description |
| --- | --- | --- |
| [Get FSPay Token](actions/get-fspay-token.md) | GET | Retrieves an FSPay token from Launch27. |

### General Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get General Settings](actions/get-general-settings.md) | GET | Retrieves general settings from Launch27. |

### Gift Card

| Action | Method | Description |
| --- | --- | --- |
| [Purchase Gift Card](actions/purchase-gift-card.md) | POST | Creates a new gift card purchase in Launch27. |

### Gift Card Discount

| Action | Method | Description |
| --- | --- | --- |
| [Check Gift Card Discount](actions/check-gift-card-discount.md) | GET | Checks a gift card discount in Launch27. |

### Invite Teams Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Invite Teams Policy](actions/get-invite-teams-policy.md) | GET | Retrieves an invite teams policy from Launch27. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Search Booking Location](actions/search-booking-location.md) | GET | Finds a booking location in Launch27. |

### Location Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Location Policy](actions/get-location-policy.md) | GET | Retrieves a location policy from Launch27. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Create Quote](actions/create-quote.md) | POST | Creates a new quote in Launch27. |

### Quote Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Quote Custom Fields](actions/get-quote-custom-fields.md) | GET | Retrieves quote custom fields from Launch27. |

### Quote Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Quote Form](actions/get-quote-form.md) | GET | Retrieves a quote form from Launch27. |

### Recurring Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Recurring Policy](actions/get-recurring-policy.md) | GET | Retrieves a recurring policy from Launch27. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Services](actions/list-booking-services.md) | GET | Retrieves booking services from Launch27. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings](actions/get-settings.md) | GET | Retrieves settings from Launch27. |

