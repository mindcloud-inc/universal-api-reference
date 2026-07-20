# Channex: Native API Reference

A consolidated summary of Channex's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.channex.io/api-v.1-documentation/api-reference
- **API base URL:** `https://staging.channex.io/api/v1`

## Authentication

### API Key

Authenticate Channex requests with a user API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.channex.io/application-documentation/api-key-access)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The current page number is read from `meta.page`.

## Pagination

Use `pagination[limit]` in the query string to set the page size (default 10; maximum 100). Use `pagination[page]` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Booking Revision](actions/acknowledge-booking-revision.md) | `POST /booking_revisions/:id/ack` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#acknowledge-booking-revision-receiving) |
| [Cancel Booking Due Invalid Card](actions/cancel-booking-due-invalid-card.md) | `POST /bookings/:bookingId/cancel_due_invalid_card` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#cancel-due-invalid-card-report-api) |
| [Create Channel Availability Rule](actions/create-channel-availability-rule.md) | `POST /channel_availability_rules` | [docs](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#create-availability-rule) |
| [Create Property](actions/create-property.md) | `POST /properties` | [docs](https://docs.channex.io/api-v.1-documentation/hotels-collection#create-property) |
| [Create Rate Plan](actions/create-rate-plan.md) | `POST /rate_plans` | [docs](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#create-rate-plan) |
| [Create Room Type](actions/create-room-type.md) | `POST /room_types` | [docs](https://docs.channex.io/api-v.1-documentation/room-types-collection#create-room-type) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.channex.io/api-v.1-documentation/webhook-collection#create-webhook) |
| [Delete Channel Availability Rule](actions/delete-channel-availability-rule.md) | `DELETE /channel_availability_rules/:id` | [docs](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#remove-availability-rule) |
| [Delete Rate Plan](actions/delete-rate-plan.md) | `DELETE /rate_plans/:id` | [docs](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#remove-rate-plan) |
| [Delete Room Type](actions/delete-room-type.md) | `DELETE /room_types/:id` | [docs](https://docs.channex.io/api-v.1-documentation/room-types-collection#remove-room-type) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://docs.channex.io/api-v.1-documentation/webhook-collection#remove-webhook) |
| [Get Availability](actions/get-availability.md) | `GET /availability` | [docs](https://docs.channex.io/api-v.1-documentation/ari#get-availability-per-room-type) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/:id` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#get-booking-by-id) |
| [Get Booking Revision](actions/get-booking-revision.md) | `GET /booking_revisions/:id` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#get-booking-revision-by-id) |
| [Get Booking Revision Feed](actions/get-booking-revision-feed.md) | `GET /booking_revisions/feed` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#booking-revisions-feed) |
| [Get Channel Availability Rule](actions/get-channel-availability-rule.md) | `GET /channel_availability_rules/:id` | [docs](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#get-availability-rule-by-id) |
| [Get Property](actions/get-property.md) | `GET /properties/:id` | [docs](https://docs.channex.io/api-v.1-documentation/hotels-collection#get-property-by-id) |
| [Get Rate Plan](actions/get-rate-plan.md) | `GET /rate_plans/:id` | [docs](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#get-rate-plan-by-id) |
| [Get Restrictions](actions/get-restrictions.md) | `GET /restrictions` | [docs](https://docs.channex.io/api-v.1-documentation/ari#get-availability-or-restrictions-per-rate-plan) |
| [Get Room Type](actions/get-room-type.md) | `GET /room_types/:id` | [docs](https://docs.channex.io/api-v.1-documentation/room-types-collection#get-room-type-by-id) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://docs.channex.io/api-v.1-documentation/webhook-collection#get-webhook-by-id) |
| [List Booking Revisions](actions/list-booking-revisions.md) | `GET /booking_revisions` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#booking-revisions-list) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#bookings-list) |
| [List Channel Availability Rules](actions/list-channel-availability-rules.md) | `GET /channel_availability_rules` | [docs](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#get-list-of-availabilty-rules) |
| [List Properties](actions/list-properties.md) | `GET /properties` | [docs](https://docs.channex.io/api-v.1-documentation/hotels-collection#properties-list) |
| [List Property Options](actions/list-property-options.md) | `GET /properties/options` | [docs](https://docs.channex.io/api-v.1-documentation/hotels-collection#property-options) |
| [List Rate Plan Options](actions/list-rate-plan-options.md) | `GET /rate_plans/options` | [docs](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#rate-plan-options) |
| [List Rate Plans](actions/list-rate-plans.md) | `GET /rate_plans` | [docs](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#rate-plans-list) |
| [List Room Type Options](actions/list-room-type-options.md) | `GET /room_types/options` | [docs](https://docs.channex.io/api-v.1-documentation/room-types-collection#room-type-options) |
| [List Room Types](actions/list-room-types.md) | `GET /room_types` | [docs](https://docs.channex.io/api-v.1-documentation/room-types-collection#room-types-list) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.channex.io/api-v.1-documentation/webhook-collection#webhooks-list) |
| [Report Booking Invalid Card](actions/report-booking-invalid-card.md) | `POST /bookings/:bookingId/invalid_card` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#invalid-card-report-api) |
| [Report Booking No Show](actions/report-booking-no-show.md) | `POST /bookings/:bookingId/no_show` | [docs](https://docs.channex.io/api-v.1-documentation/bookings-collection#no-show-report-api) |
| [Update Availability](actions/update-availability.md) | `POST /availability` | [docs](https://docs.channex.io/api-v.1-documentation/ari#update-availability) |
| [Update Channel Availability Rule](actions/update-channel-availability-rule.md) | `PUT /channel_availability_rules/:id` | [docs](https://docs.channex.io/api-v.1-documentation/availability-rules-collection#update-availability-rule) |
| [Update Property](actions/update-property.md) | `PUT /properties/:id` | [docs](https://docs.channex.io/api-v.1-documentation/hotels-collection#update-property) |
| [Update Rate Plan](actions/update-rate-plan.md) | `PUT /rate_plans/:id` | [docs](https://docs.channex.io/api-v.1-documentation/rate-plans-collection#update-rate-plan) |
| [Update Restrictions](actions/update-restrictions.md) | `POST /restrictions` | [docs](https://docs.channex.io/api-v.1-documentation/ari#update-rate-and-restrictions) |
| [Update Room Type](actions/update-room-type.md) | `PUT /room_types/:id` | [docs](https://docs.channex.io/api-v.1-documentation/room-types-collection#update-room-type) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:id` | [docs](https://docs.channex.io/api-v.1-documentation/webhook-collection#update-webhook) |
