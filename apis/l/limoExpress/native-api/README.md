# LimoExpress: Native API Reference

A consolidated summary of LimoExpress's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://api.limoexpress.me/api/docs/v1
- **OpenAPI specification:** https://api.limoexpress.me/docs?api-docs.json
- **API base URL:** `https://api.limoexpress.me`

## Authentication

### Bearer Token

Use the LimoExpress API token from advanced settings. Enter the raw token value only (without `Bearer ` prefix).

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.limoexpress.me/docs?api-docs.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Currency](actions/add-currency.md) | `POST /api/integration/add-currency` | [docs](https://api.limoexpress.me/api/docs/v1#/Currencies/addACurrency) |
| [Create Booking](actions/create-booking.md) | `PUT /api/integration/bookings` | [docs](https://api.limoexpress.me/api/docs/v1#/Bookings/createBooking) |
| [Create Booking from Website](actions/create-booking-from-website.md) | `PUT /api/integration/booking-with-fees` | [docs](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/createBookingFromWebsite) |
| [Create Client](actions/create-client.md) | `PUT /api/integration/clients` | [docs](https://api.limoexpress.me/api/docs/v1#/Clients/createAOrganisationClient) |
| [Create Payment Method](actions/create-payment-method.md) | `PUT /api/integration/payment-methods` | [docs](https://api.limoexpress.me/api/docs/v1#/Payment%20Methods/createAOrganisationPaymentMethod) |
| [Create Vehicle](actions/create-vehicle.md) | `PUT /api/integration/vehicles` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicles/createAOrganisationVehicle) |
| [Create Vehicle Class](actions/create-vehicle-class.md) | `PUT /api/integration/vehicle-classes` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/createAOrganisationVehicleClass) |
| [Delete Client](actions/delete-client.md) | `DELETE /api/integration/clients` | [docs](https://api.limoexpress.me/api/docs/v1#/Clients/deleteAOrganisationClient) |
| [Delete Payment Method](actions/delete-payment-method.md) | `DELETE /api/integration/payment-methods` | [docs](https://api.limoexpress.me/api/docs/v1#/Payment%20Methods/deleteAOrganisationPaymentMethod) |
| [Delete Vehicle](actions/delete-vehicle.md) | `DELETE /api/integration/vehicles` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicles/deleteAOrganisationVehicle) |
| [Delete Vehicle Class](actions/delete-vehicle-class.md) | `DELETE /api/integration/vehicle-classes` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/deleteAOrganisationVehicleClass) |
| [Get Extra Fees Pricing](actions/get-extra-fees-pricing.md) | `GET /api/integration/extra-fees-pricing/:currencyId/:vehicleClassId` | [docs](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/getExtraFeesPricing) |
| [Get Pricing](actions/get-pricing.md) | `GET /api/integration/pricing` | [docs](https://api.limoexpress.me/api/docs/v1#/Pricing/getPricing) |
| [Get Pricing By Vehicle Classes](actions/get-pricing-by-vehicle-classes.md) | `POST /api/integration/pricing-by-vehicle-classes` | [docs](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/getPricingByVehicleClass) |
| [List All Currencies](actions/list-all-currencies.md) | `GET /api/integration/all-currencies` | [docs](https://api.limoexpress.me/api/docs/v1#/Currencies/getAllCurrencies) |
| [List Booking Offers](actions/list-booking-offers.md) | `GET /api/integration/booking-offers` | [docs](https://api.limoexpress.me/api/docs/v1#/Booking%20Offers/getAllBookingOffers) |
| [List Booking Statuses](actions/list-booking-statuses.md) | `GET /api/integration/booking-statuses` | [docs](https://api.limoexpress.me/api/docs/v1#/Bookings/getAllBookingStatuses) |
| [List Booking Types](actions/list-booking-types.md) | `GET /api/integration/booking-types` | [docs](https://api.limoexpress.me/api/docs/v1#/Bookings/getAllBookingTypes) |
| [List Bookings](actions/list-bookings.md) | `GET /api/integration/bookings` | [docs](https://api.limoexpress.me/api/docs/v1#/Bookings/getAllBookings) |
| [List Clients](actions/list-clients.md) | `GET /api/integration/clients` | [docs](https://api.limoexpress.me/api/docs/v1#/Clients/getAllClients) |
| [List Countries](actions/list-countries.md) | `GET /api/integration/countries` | [docs](https://api.limoexpress.me/api/docs/v1#/Countries/getAllCountries) |
| [List Currencies](actions/list-currencies.md) | `GET /api/integration/currencies` | [docs](https://api.limoexpress.me/api/docs/v1#/Currencies/getAllOrganisationCurrencies) |
| [List Expenses](actions/list-expenses.md) | `GET /api/integration/expenses` | [docs](https://api.limoexpress.me/api/docs/v1#/Expenses/getAllExpenses) |
| [List Invoices](actions/list-invoices.md) | `GET /api/integration/invoices` | [docs](https://api.limoexpress.me/api/docs/v1#/Invoices/getAllInvoices) |
| [List Passengers](actions/list-passengers.md) | `GET /api/integration/passengers` | [docs](https://api.limoexpress.me/api/docs/v1#/Passengers/getAllPassengers) |
| [List Payment Methods](actions/list-payment-methods.md) | `GET /api/integration/payment-methods` | [docs](https://api.limoexpress.me/api/docs/v1#/Payment%20Methods/getAllPaymentMethods) |
| [List Users](actions/list-users.md) | `GET /api/integration/users` | [docs](https://api.limoexpress.me/api/docs/v1#/Users/getAllUsers) |
| [List Vehicle Classes](actions/list-vehicle-classes.md) | `GET /api/integration/vehicle-classes` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/getAllOrganisationVehicleClasses) |
| [List Vehicles](actions/list-vehicles.md) | `GET /api/integration/vehicles` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicles/getAllOrganisationVehicles) |
| [Mark Booking As Confirmed](actions/mark-booking-as-confirmed.md) | `POST /api/integration/mark-booking-as-confirmed` | [docs](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/markBookingAsConfirmed) |
| [Mark Booking As Paid](actions/mark-booking-as-paid.md) | `POST /api/integration/mark-booking-as-paid` | [docs](https://api.limoexpress.me/api/docs/v1#/Website%20Integration/markBookingAsPaid) |
| [Mark Booking Offer As Paid](actions/mark-booking-offer-as-paid.md) | `POST /api/integration/booking-offers/mark-as-paid` | [docs](https://api.limoexpress.me/api/docs/v1#/Booking%20Offers/markBookingOfferAsPaid) |
| [Mark Invoice As Paid](actions/mark-invoice-as-paid.md) | `POST /api/integration/invoices/mark-as-paid` | [docs](https://api.limoexpress.me/api/docs/v1) |
| [Remove Currency](actions/remove-currency.md) | `POST /api/integration/remove-currency` | [docs](https://api.limoexpress.me/api/docs/v1#/Currencies/removeACurrency) |
| [Update Booking](actions/update-booking.md) | `POST /api/integration/bookings` | [docs](https://api.limoexpress.me/api/docs/v1#/Bookings/updateBooking) |
| [Update Client](actions/update-client.md) | `POST /api/integration/clients` | [docs](https://api.limoexpress.me/api/docs/v1#/Clients/updateAOrganisationClient) |
| [Update Payment Method](actions/update-payment-method.md) | `POST /api/integration/payment-methods` | [docs](https://api.limoexpress.me/api/docs/v1#/Payment%20Methods/updateAOrganisationPaymentMethod) |
| [Update Vehicle](actions/update-vehicle.md) | `POST /api/integration/vehicles` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicles/updateAOrganisationVehicle) |
| [Update Vehicle Class](actions/update-vehicle-class.md) | `POST /api/integration/vehicle-classes` | [docs](https://api.limoexpress.me/api/docs/v1#/Vehicle%20Classes/updateAOrganisationVehicleClass) |
