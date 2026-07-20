# Bokun: Native API Reference

A consolidated summary of Bokun's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.bokun.dev/rest-v2
- **OpenAPI specification:** https://api-docs.bokun.dev/rest-v2.yaml
- **API base URL:** `https://api.bokun.io`

## Authentication

### OAuth2

OAuth2 authorization code flow for Bokun custom or public apps.

### Credentials

- **Vendor Domain:** `domain` · required · Enter the Bokun vendor domain slug used in Bokun OAuth and API URLs, for example mytours.
- **API Key:** `clientId` · required · Bokun calls the OAuth client ID the API key.
- **API Secret:** `clientSecret` · required · Bokun calls the OAuth client secret the API secret.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.domain}}.bokun.io/appstore/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.authorizeRequest.domain}}.bokun.io/appstore/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `VENDOR_USERS_READ,BOOKINGS_READ,BOOKINGS_WRITE,CHECKOUTS_READ,CHECKOUTS_WRITE,CUSTOMERS_READ,CUSTOMERS_WRITE,CUSTOMERS_CONTACT_READ,PRODUCTS_READ,PRODUCTS_WRITE,PRODUCT_AVAILABILITY_WRITE,PRODUCT_PRICING_WRITE,BOOKING_CHANNELS_READ`.

[Official authentication documentation](https://bokun.dev/api/uzi4nXgs2wN1DhxkkLHves/authenticate-with-oauth/jfrEPmAX72TCXxgTZTWiG3)

### API Key (Signed REST)

Bokun Booking API authentication using access key, secret key, and request signing headers.

### Credentials

- **Access Key:** `accessKey` · required · The Bokun access key from the API key pair.
- **Secret Key:** `secretKey` · required · The Bokun secret key used to sign Booking API requests.

[Official authentication documentation](https://bokun.dev/booking-api-rest/vU6sCfxwYdJWd1QAcLt12i/configuring-the-platform-for-api-usage-and-authentication/sFiGRpo4detkmrZPcWtQPj)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json;charset=UTF-8` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Booking Audit Trail](actions/get-booking-audit-trail.md) | `GET /restapi/v2.0/booking/:bookingId/audit-records` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Booking Payments](actions/get-booking-payments.md) | `GET /restapi/v2.0/booking/:bookingId/payments` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Customer](actions/get-customer.md) | `GET /restapi/v2.0/customer/:customerId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Price Schedule](actions/get-price-schedule.md) | `GET /restapi/v2.0/pricing/schedule/:priceScheduleId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Pricing Category](actions/get-pricing-category.md) | `GET /restapi/v2.0/pricing/category/:pricingCategoryId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Promo Code](actions/get-promo-code.md) | `GET /restapi/v2.0/promo/code/:promoCodeId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Resource](actions/get-resource.md) | `GET /restapi/v2.0/resource/:resourceId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Resource Pool](actions/get-resource-pool.md) | `GET /restapi/v2.0/resource/pool/:resourcePoolId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [Get Tax](actions/get-tax.md) | `GET /restapi/v2.0/tax/:taxId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Cancellation Policies](actions/list-cancellation-policies.md) | `GET /restapi/v2.0/cancellation/policies` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Countries](actions/list-countries.md) | `GET /restapi/v2.0/countries` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Experience Availability](actions/list-experience-availability.md) | `GET /restapi/v2.0/availability/:experienceId` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Experience Availability Statistics](actions/list-experience-availability-statistics.md) | `GET /restapi/v2.0/availability/:experienceId/statistics` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Experience Booking Notes](actions/list-experience-booking-notes.md) | `GET /restapi/v2.0/experienceBooking/:experienceBookingId/notes` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Experience Closeouts](actions/list-experience-closeouts.md) | `GET /restapi/v2.0/availability/:experienceId/closeouts` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Experience IDs](actions/list-experience-ids.md) | `GET /restapi/v2.0/experiences/ids` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Price Catalogs](actions/list-price-catalogs.md) | `GET /restapi/v2.0/price/catalogs` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Price Schedules](actions/list-price-schedules.md) | `GET /restapi/v2.0/pricing/schedules` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Pricing Categories](actions/list-pricing-categories.md) | `GET /restapi/v2.0/pricing/categories` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Promo Codes](actions/list-promo-codes.md) | `GET /restapi/v2.0/promo/codes` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Resource Pools](actions/list-resource-pools.md) | `GET /restapi/v2.0/resource/pools` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Resources](actions/list-resources.md) | `GET /restapi/v2.0/resources` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Taxes](actions/list-taxes.md) | `GET /restapi/v2.0/taxes` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
| [List Time Zones](actions/list-time-zones.md) | `GET /restapi/v2.0/timezones` | [docs](https://api-docs.bokun.dev/rest-v2.yaml) |
