# <img src="https://images.mindcloud.co/apps/icons/unnamed-7_1774457606839.png" alt="Edoobox logo" width="28" height="28"> Edoobox: Universal API

Manage edoobox offers and bookings.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/edoobox/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.edoobox.com
- **Vendor API docs:** https://api.docs.edoobox.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Booking](actions/get-booking.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-booking?connectionId=$CONNECTION_ID&bookingId=booking_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in Edoobox. |
| [Get Booking](actions/get-booking.md) | GET | Retrieves details for a booking from Edoobox. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves a list of bookings from Edoobox. |

### Booking Cancellation

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | PUT | Cancels an existing booking in Edoobox. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Edoobox. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from Edoobox. |
| [Get Category](actions/get-category.md) | GET | Retrieves details for a category from Edoobox. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves a list of categories from Edoobox. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Edoobox. |

### Category Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Get Category Dashboard](actions/get-category-dashboard.md) | GET | Retrieves a category dashboard from Edoobox. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Edoobox. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves details for an invoice from Edoobox. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from Edoobox. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Edoobox. |
| [List Notes](actions/list-notes.md) | GET | Retrieves a list of notes from Edoobox. |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Create Offer](actions/create-offer.md) | POST | Creates a new offer in Edoobox. |
| [Get Offer](actions/get-offer.md) | GET | Retrieves details for an offer from Edoobox. |
| [List Offers](actions/list-offers.md) | GET | Retrieves a list of offers from Edoobox. |
| [Update Offer](actions/update-offer.md) | PUT | Updates an existing offer in Edoobox. |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [Copy Offer](actions/copy-offer.md) | POST | Copies an existing offer in Edoobox, with or without dates. |
| [Delete Offer](actions/delete-offer.md) | DELETE | Deletes an existing offer from Edoobox. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves a list of transactions from Edoobox. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Edoobox. |
| [Get User Dashboard](actions/get-user-dashboard.md) | GET | Retrieves a user dashboard from Edoobox. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Edoobox. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Edoobox. |
| [Get User](actions/get-user.md) | GET | Retrieves details for a user from Edoobox. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Edoobox. |

### Vat

| Action | Method | Description |
| --- | --- | --- |
| [Get Vat](actions/get-vat.md) | GET | Retrieves details for a VAT rate from Edoobox. |
| [List Vats](actions/list-vats.md) | GET | Retrieves a list of VAT rates from Edoobox. |

