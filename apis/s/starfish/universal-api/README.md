# <img src="https://images.mindcloud.co/apps/icons/camping-care_1775759956367.png" alt="Starfish logo" width="28" height="28"> Starfish: Universal API

Manage reservations, guests, accommodations, invoices, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/starfish/latest
- **Category:** Support / Field Service
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.camping.care
- **Vendor API docs:** https://developer.camping.care/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Accommodation

| Action | Method | Description |
| --- | --- | --- |
| [Create Accommodation](actions/create-accommodation.md) | POST | Creates a new accommodation in Starfish. |
| [Delete Accommodation](actions/delete-accommodation.md) | DELETE | Deletes an existing accommodation from Starfish. |
| [Get Accommodation](actions/get-accommodation.md) | GET | Retrieves a specific accommodation from Starfish. |
| [List Accommodations](actions/list-accommodations.md) | GET | Retrieves a list of accommodations from Starfish. |
| [Update Accommodation](actions/update-accommodation.md) | PUT | Updates an existing accommodation in Starfish. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Starfish. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Starfish. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from Starfish. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from Starfish. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Starfish. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Starfish. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Starfish. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves a specific invoice from Starfish. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from Starfish. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Starfish. |

### Place

| Action | Method | Description |
| --- | --- | --- |
| [Create Place](actions/create-place.md) | POST | Creates a new place in a Starfish accommodation. |
| [Get Place](actions/get-place.md) | GET | Retrieves a specific place from a Starfish accommodation. |
| [List Places](actions/list-places.md) | GET | Retrieves places for a specific accommodation in Starfish. |
| [Update Place](actions/update-place.md) | PUT | Updates an existing place in a Starfish accommodation. |

### Reservation

| Action | Method | Description |
| --- | --- | --- |
| [Create Reservation](actions/create-reservation.md) | POST | Creates a new reservation in Starfish. |
| [Get Reservation](actions/get-reservation.md) | GET | Retrieves a specific reservation from Starfish. |
| [List Reservations](actions/list-reservations.md) | GET | Retrieves a list of reservations from Starfish. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current authenticated user from Starfish. |

