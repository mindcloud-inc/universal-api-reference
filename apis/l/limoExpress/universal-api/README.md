# <img src="https://images.mindcloud.co/apps/icons/limo-express_1775146198162.png" alt="LimoExpress logo" width="28" height="28"> LimoExpress: Universal API

LimoExpress dispatch and booking platform API for bookings, vehicles, clients, invoices, and related transportation operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/limoExpress/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.limoexpress.me/
- **Vendor API docs:** https://api.limoexpress.me/api/docs/v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Booking Statuses](actions/list-booking-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-booking-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in LimoExpress. |
| [Create Booking from Website](actions/create-booking-from-website.md) | POST | Creates a website booking in LimoExpress. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from the LimoExpress organization. |
| [Mark Booking As Confirmed](actions/mark-booking-as-confirmed.md) | PUT | Marks a booking as confirmed in LimoExpress. |
| [Mark Booking As Paid](actions/mark-booking-as-paid.md) | PUT | Marks a booking as paid in LimoExpress. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in LimoExpress. |

### Booking Offer

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Offers](actions/list-booking-offers.md) | GET | Retrieves booking offers from the LimoExpress organization. |
| [Mark Booking Offer As Paid](actions/mark-booking-offer-as-paid.md) | PUT | Marks a booking offer as paid in LimoExpress. |

### Booking Status

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Statuses](actions/list-booking-statuses.md) | GET | Retrieves booking statuses from the LimoExpress organization. |

### Booking Type

| Action | Method | Description |
| --- | --- | --- |
| [List Booking Types](actions/list-booking-types.md) | GET | Retrieves booking types from the LimoExpress organization. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in LimoExpress. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from LimoExpress. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from the LimoExpress organization. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in LimoExpress. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from the LimoExpress platform. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [Add Currency](actions/add-currency.md) | POST | Adds a currency to the LimoExpress organization. |
| [List All Currencies](actions/list-all-currencies.md) | GET | Retrieves all currencies from the LimoExpress platform. |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves organization currencies from the LimoExpress platform. |
| [Remove Currency](actions/remove-currency.md) | DELETE | Removes a currency from the LimoExpress organization. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from the LimoExpress organization. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from the LimoExpress organization. |
| [Mark Invoice As Paid](actions/mark-invoice-as-paid.md) | PUT |  |

### Passenger

| Action | Method | Description |
| --- | --- | --- |
| [List Passengers](actions/list-passengers.md) | GET | Retrieves passengers from the LimoExpress organization. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Method](actions/create-payment-method.md) | POST | Creates a new payment method in LimoExpress. |
| [Delete Payment Method](actions/delete-payment-method.md) | DELETE | Deletes an existing payment method from LimoExpress. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from the LimoExpress organization. |
| [Update Payment Method](actions/update-payment-method.md) | PUT | Updates an existing payment method in LimoExpress. |

### Pricing

| Action | Method | Description |
| --- | --- | --- |
| [Get Extra Fees Pricing](actions/get-extra-fees-pricing.md) | GET | Retrieves extra fee pricing in LimoExpress by currency and vehicle class. |
| [Get Pricing](actions/get-pricing.md) | GET | Retrieves pricing for coordinates in LimoExpress. |
| [Get Pricing By Vehicle Classes](actions/get-pricing-by-vehicle-classes.md) | GET | Retrieves pricing by vehicle class in LimoExpress. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from the LimoExpress organization. |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle](actions/create-vehicle.md) | POST | Creates a new vehicle in LimoExpress. |
| [Delete Vehicle](actions/delete-vehicle.md) | DELETE | Deletes an existing vehicle from LimoExpress. |
| [List Vehicles](actions/list-vehicles.md) | GET | Retrieves vehicles from the LimoExpress organization. |
| [Update Vehicle](actions/update-vehicle.md) | PUT | Updates an existing vehicle in LimoExpress. |

### Vehicle Class

| Action | Method | Description |
| --- | --- | --- |
| [Create Vehicle Class](actions/create-vehicle-class.md) | POST | Creates a new vehicle class in LimoExpress. |
| [Delete Vehicle Class](actions/delete-vehicle-class.md) | DELETE | Deletes an existing vehicle class from LimoExpress. |
| [List Vehicle Classes](actions/list-vehicle-classes.md) | GET | Retrieves vehicle classes from the LimoExpress organization. |
| [Update Vehicle Class](actions/update-vehicle-class.md) | PUT | Updates an existing vehicle class in LimoExpress. |

