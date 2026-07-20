# Eventix: Native API Reference

A consolidated summary of Eventix's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.weeztix.com/api/
- **OpenAPI specification:** https://eventix-docs.s3.eu-west-1.amazonaws.com/dashboard
- **API base URL:** `https://api.weeztix.com`

## Authentication

### OAuth2

OAuth2 authorization-code authentication for the Weeztix API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.weeztix.com/login to approve access.
2. Exchange the returned authorization code with a POST request to https://auth.weeztix.com/tokens.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://auth.weeztix.com/tokens.

[Official authentication documentation](https://docs.weeztix.com/docs/introduction/authentication/)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get a specific Coupon](actions/get-coupon-specific.md) | `GET /3.0.0/coupon/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-coupon-specific) |
| [Get Coupons](actions/get-coupons.md) | `GET /3.0.0/coupon/:type` | [docs](https://docs.weeztix.com/api/dashboard/get-coupons) |
| [Get a specific EventDate](actions/get-event-date-specific.md) | `GET /3.0.0/eventdate/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-event-date-specific) |
| [Retrieve the Event of an EventDate](actions/get-event-date-specific-event.md) | `GET /3.0.0/eventdate/:guid/event` | [docs](https://docs.weeztix.com/api/dashboard/get-event-date-specific-event) |
| [Retrieve the Location of an EventDate](actions/get-event-date-specific-location.md) | `GET /3.0.0/eventdate/:guid/location` | [docs](https://docs.weeztix.com/api/dashboard/get-event-date-specific-location) |
| [Get EventDates](actions/get-event-dates.md) | `GET /3.0.0/eventdate/:type` | [docs](https://docs.weeztix.com/api/dashboard/get-event-dates) |
| [Retrieve a specific Location](actions/get-event-location-specific.md) | `GET /3.0.0/location/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-event-location-specific) |
| [Get EventDates for specific Location](actions/get-event-location-specific-event-dates.md) | `GET /3.0.0/location/:guid/dates` | [docs](https://docs.weeztix.com/api/dashboard/get-event-location-specific-event-dates) |
| [Get Locations](actions/get-event-locations.md) | `GET /3.0.0/location/:type` | [docs](https://docs.weeztix.com/api/dashboard/get-event-locations) |
| [Get a specific Event](actions/get-event-specific.md) | `GET /3.0.0/event/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific) |
| [Get analysis of an Event](actions/get-event-specific-analysis.md) | `GET /3.0.0/event/:guid/analysis` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific-analysis) |
| [Get EventDates for Event](actions/get-event-specific-event-dates.md) | `GET /3.0.0/event/:guid/dates` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific-event-dates) |
| [Get EventDates for Event with Products](actions/get-event-specific-event-dates-with-products.md) | `GET /3.0.0/event/:guid/dates/products` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific-event-dates-with-products) |
| [Get Location of Event](actions/get-event-specific-event-location.md) | `GET /3.0.0/event/:guid/location` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific-event-location) |
| [Get Scanning stats for an event](actions/get-event-specific-scanning-stats.md) | `GET /3.0.0/event/:guid/scanningstats` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific-scanning-stats) |
| [Get all Shops of an Event](actions/get-event-specific-shops.md) | `GET /3.0.0/event/:guid/shops` | [docs](https://docs.weeztix.com/api/dashboard/get-event-specific-shops) |
| [Get Ticket Types for Event](actions/get-event-tickets.md) | `GET /3.0.0/event/:guid/ticket/:type` | [docs](https://docs.weeztix.com/api/dashboard/get-event-tickets) |
| [Get Ticket Types for Event with Products](actions/get-event-tickets-with-products.md) | `GET /3.0.0/event/:guid/ticket/products` | [docs](https://docs.weeztix.com/api/dashboard/get-event-tickets-with-products) |
| [Get Ticket Types for Event with Shops](actions/get-event-tickets-with-shops.md) | `GET /3.0.0/event/:guid/ticket/shops` | [docs](https://docs.weeztix.com/api/dashboard/get-event-tickets-with-shops) |
| [Get Events](actions/get-events.md) | `GET /3.0.0/event/:type` | [docs](https://docs.weeztix.com/api/dashboard/get-events) |
| [Get an entire specific Order](actions/get-order-specific.md) | `GET /3.0.0/order/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-order-specific) |
| [Get specific Product Type](actions/get-product-specific.md) | `GET /3.0.0/product/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-product-specific) |
| [Get attached EventDates of Product Type](actions/get-product-specific-event-dates.md) | `GET /3.0.0/product/:guid/dates` | [docs](https://docs.weeztix.com/api/dashboard/get-product-specific-event-dates) |
| [Get attached Metadata of Product Type](actions/get-product-specific-metadata.md) | `GET /3.0.0/product/:guid/metaData` | [docs](https://docs.weeztix.com/api/dashboard/get-product-specific-metadata) |
| [Get Ticket Types of Product Type](actions/get-product-specific-tickets.md) | `GET /3.0.0/product/:guid/tickets` | [docs](https://docs.weeztix.com/api/dashboard/get-product-specific-tickets) |
| [Get a specific Shop](actions/get-shop-specific.md) | `GET /3.0.0/shop/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific) |
| [Get attached Metadata of Shop](actions/get-shop-specific-metadata.md) | `GET /3.0.0/shop/:guid/metadata` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific-metadata) |
| [Get a specific Shop's options](actions/get-shop-specific-options.md) | `GET /3.0.0/shop/:guid/options` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific-options) |
| [Get attached PaymentMethods of Shop](actions/get-shop-specific-payment-methods.md) | `GET /3.0.0/shop/:guid/payment_methods` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific-payment-methods) |
| [Get attached Products of Shop](actions/get-shop-specific-product.md) | `GET /3.0.0/shop/:guid/products` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific-product) |
| [Get attached ShopTrackers of Shop](actions/get-shop-specific-shop-trackers.md) | `GET /3.0.0/shop/:guid/trackers` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific-shop-trackers) |
| [Get attached Ticket Types of Shop](actions/get-shop-specific-ticket.md) | `GET /3.0.0/shop/:guid/tickets` | [docs](https://docs.weeztix.com/api/dashboard/get-shop-specific-ticket) |
| [Get Shops](actions/get-shops.md) | `GET /3.0.0/shop/:type` | [docs](https://docs.weeztix.com/api/dashboard/get-shops) |
| [Get a specific Ticket Type](actions/get-ticket-specific.md) | `GET /3.0.0/ticket/:guid` | [docs](https://docs.weeztix.com/api/dashboard/get-ticket-specific) |
| [Get attached EventDates of Ticket Type](actions/get-ticket-specific-event-dates.md) | `GET /3.0.0/ticket/:guid/dates` | [docs](https://docs.weeztix.com/api/dashboard/get-ticket-specific-event-dates) |
| [Get all ProductGroups for this Ticket Type](actions/get-ticket-specific-product-groups.md) | `GET /3.0.0/ticket/:guid/groups` | [docs](https://docs.weeztix.com/api/dashboard/get-ticket-specific-product-groups) |
| [Get all ProductGroups with Product Types for this Ticket Type](actions/get-ticket-specific-product-groups-with-products.md) | `GET /3.0.0/ticket/:guid/groups/products` | [docs](https://docs.weeztix.com/api/dashboard/get-ticket-specific-product-groups-with-products) |
| [Retrieve all Product Types attached to this Ticket Type](actions/get-ticket-specific-products.md) | `GET /3.0.0/ticket/:guid/products` | [docs](https://docs.weeztix.com/api/dashboard/get-ticket-specific-products) |
| [Get Order status link](actions/search-order-by-payment-id.md) | `GET /3.0.0/order/search/:payment_id` | [docs](https://docs.weeztix.com/api/dashboard/search-order-by-payment-id) |
| [Get all Shops this Ticket Type is attached to](actions/ticket-list-shops.md) | `GET /3.0.0/ticket/:guid/shops` | [docs](https://docs.weeztix.com/api/dashboard/ticket-list-shops) |
