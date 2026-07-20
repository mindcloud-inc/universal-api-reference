# <img src="https://images.mindcloud.co/apps/icons/planyo_1774033214184.png" alt="Planyo logo" width="28" height="28"> Planyo: Universal API

Manage Planyo reservations, resources, users, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/planyo/latest
- **Category:** Productivity / Scheduling
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.planyo.com
- **Vendor API docs:** https://www.planyo.com/api.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site Info](actions/get-site-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Event Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Times](actions/get-event-times.md) | GET | Retrieves event times from Planyo. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from Planyo. |

### Rental Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Rental Price](actions/get-rental-price.md) | GET | Retrieves a rental price from Planyo. |

### Reservation

| Action | Method | Description |
| --- | --- | --- |
| [Create Reservation](actions/create-reservation.md) | POST | Creates a new reservation in Planyo. |
| [Delete Reservation](actions/delete-reservation.md) | DELETE | Deletes an existing reservation from Planyo. |
| [Do Reservation Action](actions/do-reservation-action.md) | PUT | Performs a reservation action in Planyo. |
| [Get Reservation Data](actions/get-reservation-data.md) | GET | Retrieves reservation data from Planyo. |
| [List Reservations](actions/list-reservations.md) | GET | Retrieves reservations from Planyo. |
| [Update Reservation](actions/update-reservation.md) | PUT | Updates an existing reservation in Planyo. |

### Reservation Check

| Action | Method | Description |
| --- | --- | --- |
| [Can Make Reservation](actions/can-make-reservation.md) | GET | Checks whether a reservation can be made in Planyo. |

### Reservation Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Reservation Actions](actions/get-reservation-actions.md) | GET | Retrieves reservation actions from Planyo. |

### Reservation Payment

| Action | Method | Description |
| --- | --- | --- |
| [Add Reservation Payment](actions/add-reservation-payment.md) | POST | Adds a reservation payment in Planyo. |
| [List Reservation Payments](actions/list-reservation-payments.md) | GET | Retrieves reservation payments from Planyo. |
| [Remove Reservation Payment](actions/remove-reservation-payment.md) | DELETE | Deletes a reservation payment from Planyo. |
| [Update Reservation Payment](actions/update-reservation-payment.md) | PUT | Updates a reservation payment in Planyo. |

### Reservation Payment Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Reservation Payment Amount](actions/get-reservation-payment-amount.md) | GET | Retrieves a reservation payment amount from Planyo. |

### Reservation Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Reservations](actions/search-reservations.md) | GET | Finds reservations in Planyo by query. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Info](actions/get-resource-info.md) | GET | Retrieves resource information from Planyo. |
| [List Resources](actions/list-resources.md) | GET | Retrieves resources from Planyo. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Info](actions/get-site-info.md) | GET | Retrieves site information from Planyo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add User](actions/add-user.md) | POST | Creates a new user in Planyo. |
| [Get User Data](actions/get-user-data.md) | GET | Retrieves user data from Planyo. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Planyo. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Planyo. |

