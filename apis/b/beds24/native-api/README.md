# Beds24: Native API Reference

A consolidated summary of Beds24's API configuration and 51 documented operations, with links to official documentation.

- **Official docs:** https://wiki.beds24.com/index.php/API_V2.0
- **API base URL:** `https://beds24.com/api/v2`

## Authentication

### Beds24 Access Token

Authenticates Beds24 API v2 requests with the provider's `token` header using a live access token minted from a Beds24 refresh token outside MindCloud.

### Credentials

- **Access Token:** `accessToken` · optional · Current Beds24 API access token value to send in the `token` header. Generate this from a valid Beds24 refresh token before saving the connection.

Send these headers with each API request:

```http
token: <accessToken>
```

[Official authentication documentation](https://wiki.beds24.com/index.php/API_V2.0)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (51 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Stripe Payment Method](actions/add-stripe-payment-method.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Capture Stripe Charge](actions/capture-stripe-charge.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Charge Stripe Payment Method](actions/charge-stripe-payment-method.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Connect Airbnb Listing to Existing Room](actions/connect-airbnb-listing-to-existing-room.md) | `POST /channels/airbnb` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Create or Update Accounts](actions/create-or-update-accounts.md) | `POST /accounts` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Create or Update Bookings](actions/create-or-update-bookings.md) | `POST /bookings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Create or Update Fixed Prices](actions/create-or-update-fixed-prices.md) | `POST /inventory/fixedPrices` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Create or Update Properties](actions/create-or-update-properties.md) | `POST /properties` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Create Stripe Checkout Session](actions/create-stripe-checkout-session.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Delete Bookings](actions/delete-bookings.md) | `DELETE /bookings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Delete Properties](actions/delete-properties.md) | `DELETE /properties` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Delete Property Rooms](actions/delete-property-rooms.md) | `DELETE /properties/rooms` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Detach Stripe Payment Method](actions/detach-stripe-payment-method.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Disconnect Airbnb Room](actions/disconnect-airbnb-room.md) | `POST /channels/airbnb` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Get Access Token from Invite Code](actions/get-access-token-from-invite-code.md) | `GET /authentication/setup` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Get Token Details](actions/get-token-details.md) | `GET /authentication/details` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Import Airbnb Listing as New Property](actions/import-airbnb-listing-as-new-property.md) | `POST /channels/airbnb` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Import Airbnb Listing to Existing Property](actions/import-airbnb-listing-to-existing-property.md) | `POST /channels/airbnb` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Airbnb Listings](actions/list-airbnb-listings.md) | `GET /channels/airbnb/listings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Airbnb Reviews](actions/list-airbnb-reviews.md) | `GET /channels/airbnb/reviews` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Airbnb Users](actions/list-airbnb-users.md) | `GET /channels/airbnb/users` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Booking.com Reviews](actions/list-booking-com-reviews.md) | `GET /channels/booking/reviews` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Booking Invoices](actions/list-booking-invoices.md) | `GET /bookings/invoices` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Booking Messages](actions/list-booking-messages.md) | `GET /bookings/messages` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Channel Settings](actions/list-channel-settings.md) | `GET /channels/settings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Fixed Prices](actions/list-fixed-prices.md) | `GET /inventory/fixedPrices` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Organization Users](actions/list-organization-users.md) | `GET /organizations/users` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Properties](actions/list-properties-2.md) | `GET /properties` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Property Rooms](actions/list-property-rooms.md) | `GET /properties/rooms` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Room Availability](actions/list-room-availability.md) | `GET /inventory/rooms/availability` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Room Calendar](actions/list-room-calendar.md) | `GET /inventory/rooms/calendar` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Room Offers](actions/list-room-offers.md) | `GET /inventory/rooms/offers` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Room Unit Bookings](actions/list-room-unit-bookings.md) | `GET /inventory/rooms/unitBookings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Stripe Charges](actions/list-stripe-charges.md) | `GET /channels/stripe/charges` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [List Stripe Payment Methods](actions/list-stripe-payment-methods.md) | `GET /channels/stripe/paymentMethods` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Refresh Access Token](actions/refresh-access-token.md) | `GET /authentication/token` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Refund Stripe Charge](actions/refund-stripe-charge.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Release Stripe Charge](actions/release-stripe-charge.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Report Booking.com Cancellation Request](actions/report-booking-com-cancellation-request.md) | `POST /channels/booking` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Report Booking.com Invalid Card](actions/report-booking-com-invalid-card.md) | `POST /channels/booking` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Report Booking.com No Show](actions/report-booking-com-no-show.md) | `POST /channels/booking` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Revoke Refresh Token](actions/revoke-refresh-token.md) | `DELETE /authentication/token` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Run Airbnb Channel Action](actions/run-airbnb-channel-action.md) | `POST /channels/airbnb` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Run Booking.com Channel Action](actions/run-booking-channel-action.md) | `POST /channels/booking` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Run Stripe Channel Action](actions/run-stripe-channel-action.md) | `POST /channels/stripe` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Send or Mark Booking Messages](actions/send-or-mark-booking-messages.md) | `POST /bookings/messages` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Update Booking Messages](actions/update-booking-messages.md) | `PATCH /bookings/messages` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Update Channel Settings](actions/update-channel-settings.md) | `POST /channels/settings` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
| [Update Room Calendar](actions/update-room-calendar.md) | `POST /inventory/rooms/calendar` | [docs](https://wiki.beds24.com/index.php/API_V2.0) |
