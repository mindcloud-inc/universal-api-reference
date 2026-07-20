# <img src="https://images.mindcloud.co/apps/icons/beds24_1775844186171.png" alt="Beds24 logo" width="28" height="28"> Beds24: Universal API

Beds24 API v2 integration for properties, bookings, inventory, accounts, channel settings, and channel operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/beds24/latest
- **Actions:** 51
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.beds24.com
- **Vendor API docs:** https://wiki.beds24.com/index.php/API_V2.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Token Details](actions/get-token-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (51)

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [Capture Stripe Charge](actions/capture-stripe-charge.md) | PUT | Captures a Stripe charge in Beds24. |
| [Charge Stripe Payment Method](actions/charge-stripe-payment-method.md) | POST | Creates a Stripe charge from a payment method in Beds24. |
| [Release Stripe Charge](actions/release-stripe-charge.md) | PUT | Releases a Stripe charge authorization in Beds24. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Add Stripe Payment Method](actions/add-stripe-payment-method.md) | POST | Adds a Stripe payment method in Beds24. |
| [Detach Stripe Payment Method](actions/detach-stripe-payment-method.md) | DELETE | Detaches a Stripe payment method from Beds24. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Refund Stripe Charge](actions/refund-stripe-charge.md) | POST | Refunds a Stripe charge in Beds24. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Connect Airbnb Listing to Existing Room](actions/connect-airbnb-listing-to-existing-room.md) | PUT | Connects an Airbnb listing to an existing Beds24 room. |
| [Create or Update Accounts](actions/create-or-update-accounts.md) | POST | Creates or updates accounts in Beds24. |
| [Create or Update Bookings](actions/create-or-update-bookings.md) | POST | Creates or updates bookings in Beds24. |
| [Create or Update Fixed Prices](actions/create-or-update-fixed-prices.md) | POST | Creates or updates fixed prices in Beds24. |
| [Create or Update Properties](actions/create-or-update-properties.md) | POST | Creates or updates properties in Beds24. |
| [Create Stripe Checkout Session](actions/create-stripe-checkout-session.md) | POST | Creates a Stripe Checkout session in Beds24. |
| [Delete Bookings](actions/delete-bookings.md) | DELETE | Deletes bookings from Beds24 by ID. |
| [Delete Properties](actions/delete-properties.md) | DELETE | Deletes properties from Beds24. |
| [Delete Property Rooms](actions/delete-property-rooms.md) | DELETE | Deletes property rooms from Beds24. |
| [Disconnect Airbnb Room](actions/disconnect-airbnb-room.md) | DELETE | Disconnects an Airbnb room from Beds24. |
| [Get Access Token from Invite Code](actions/get-access-token-from-invite-code.md) | GET | Retrieves access and refresh tokens from a Beds24 invite code. |
| [Get Token Details](actions/get-token-details.md) | GET | Retrieves token details and diagnostics from Beds24. |
| [Import Airbnb Listing as New Property](actions/import-airbnb-listing-as-new-property.md) | POST | Imports an Airbnb listing as a new property in Beds24. |
| [Import Airbnb Listing to Existing Property](actions/import-airbnb-listing-to-existing-property.md) | PUT | Imports an Airbnb listing to an existing Beds24 property. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts and sub-accounts from Beds24. |
| [List Airbnb Listings](actions/list-airbnb-listings.md) | GET | Retrieves Airbnb listings from Beds24 by Airbnb user ID. |
| [List Airbnb Reviews](actions/list-airbnb-reviews.md) | GET | Retrieves Airbnb guest reviews from Beds24. |
| [List Airbnb Users](actions/list-airbnb-users.md) | GET | Retrieves Airbnb user IDs connected to a Beds24 account. |
| [List Booking.com Reviews](actions/list-booking-com-reviews.md) | GET | Retrieves Booking.com reviews from Beds24. |
| [List Booking Invoices](actions/list-booking-invoices.md) | GET | Retrieves booking invoices from Beds24. |
| [List Booking Messages](actions/list-booking-messages.md) | GET | Retrieves messages for a booking from Beds24. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from Beds24 by specified criteria. |
| [List Channel Settings](actions/list-channel-settings.md) | GET | Retrieves channel settings from Beds24. |
| [List Fixed Prices](actions/list-fixed-prices.md) | GET | Retrieves fixed prices from Beds24. |
| [List Organization Users](actions/list-organization-users.md) | GET | Retrieves organization users from Beds24. |
| [List Properties](actions/list-properties-2.md) | GET | Retrieves properties from Beds24. |
| [List Property Rooms](actions/list-property-rooms.md) | GET | Retrieves property rooms from Beds24. |
| [List Room Availability](actions/list-room-availability.md) | GET | Retrieves room availability dates from Beds24. |
| [List Room Calendar](actions/list-room-calendar.md) | GET | Retrieves room calendar values from Beds24. |
| [List Room Offers](actions/list-room-offers.md) | GET | Retrieves room offers from Beds24 by stay criteria. |
| [List Room Unit Bookings](actions/list-room-unit-bookings.md) | GET | Retrieves unit booking dates from Beds24. |
| [List Stripe Charges](actions/list-stripe-charges.md) | GET | Retrieves Stripe charges for a booking from Beds24. |
| [List Stripe Payment Methods](actions/list-stripe-payment-methods.md) | GET | Retrieves Stripe payment methods for a booking from Beds24. |
| [Refresh Access Token](actions/refresh-access-token.md) | GET | Retrieves an access token from a Beds24 refresh token. |
| [Report Booking.com Cancellation Request](actions/report-booking-com-cancellation-request.md) | POST | Reports a cancellation request to Booking.com from Beds24. |
| [Report Booking.com Invalid Card](actions/report-booking-com-invalid-card.md) | POST | Reports an invalid card to Booking.com from Beds24. |
| [Report Booking.com No Show](actions/report-booking-com-no-show.md) | POST | Reports a no-show to Booking.com from Beds24. |
| [Revoke Refresh Token](actions/revoke-refresh-token.md) | DELETE | Revokes a refresh token in Beds24. |
| [Run Airbnb Channel Action](actions/run-airbnb-channel-action.md) | POST | Performs an Airbnb channel action in Beds24. |
| [Run Booking.com Channel Action](actions/run-booking-channel-action.md) | POST | Performs a Booking.com channel action in Beds24. |
| [Run Stripe Channel Action](actions/run-stripe-channel-action.md) | POST | Performs a Stripe channel action in Beds24. |
| [Send or Mark Booking Messages](actions/send-or-mark-booking-messages.md) | POST | Sends booking messages or marks them as read in Beds24. |
| [Update Booking Messages](actions/update-booking-messages.md) | PUT | Updates selected booking messages in Beds24. |
| [Update Channel Settings](actions/update-channel-settings.md) | PUT | Updates channel settings in Beds24. |
| [Update Room Calendar](actions/update-room-calendar.md) | PUT | Updates room calendar values in Beds24. |

