# <img src="https://images.mindcloud.co/apps/icons/key-vox_1775066342478.png" alt="KeyVox logo" width="28" height="28"> KeyVox: Universal API

KeyVox provides smart lock, locker, access, and reservation APIs for hospitality and property operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/keyVox/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://keyvox.co
- **Vendor API docs:** https://developers.keyvox.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Units](actions/list-units.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyVox/latest/actions/list-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Lock Card](actions/create-lock-card.md) | POST | Creates a new lock card in KeyVox. |
| [Create Lock PIN](actions/create-lock-pin.md) | POST | Creates a new lock PIN in KeyVox. |
| [Create Locker PIN](actions/create-locker-pin.md) | POST | Creates a new locker PIN in KeyVox. |
| [Delete Lock Card](actions/delete-lock-card.md) | DELETE | Deletes an existing lock card from KeyVox. |
| [Delete Lock PIN](actions/delete-lock-pin.md) | DELETE | Deletes an existing lock PIN from KeyVox. |
| [Delete Locker PIN](actions/delete-locker-pin.md) | DELETE | Deletes an existing locker PIN from KeyVox. |
| [Get Lock Card Status](actions/get-lock-card-status.md) | GET | Retrieves a lock card status from KeyVox. |
| [Get Lock PIN Status](actions/get-lock-pin-status.md) | GET | Retrieves a lock PIN status from KeyVox. |
| [Issue Lock Key](actions/issue-lock-key.md) | POST | Issues a lock key for a KeyVox user. |
| [List Lock Cards](actions/list-lock-cards.md) | GET | Lists lock cards in your KeyVox account. |
| [List Lock PINs](actions/list-lock-pi-ns.md) | GET | Lists lock PINs in your KeyVox account. |
| [List Unit PINs](actions/list-unit-pi-ns.md) | GET | Lists unit PINs in your KeyVox account. |
| [Update Lock Card](actions/update-lock-card.md) | PUT | Updates an existing lock card in KeyVox. |
| [Update Lock PIN](actions/update-lock-pin.md) | PUT | Updates an existing lock PIN in KeyVox. |
| [Update Locker PIN](actions/update-locker-pin.md) | PUT | Updates an existing locker PIN in KeyVox. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get Lock Status](actions/get-lock-status.md) | GET | Retrieves a lock status from KeyVox. |
| [Get Locker Status](actions/get-locker-status.md) | GET | Retrieves a locker status from KeyVox. |
| [List Lock Events](actions/list-lock-events.md) | GET | Lists lock events in your KeyVox account. |
| [List Lock History](actions/list-lock-history.md) | GET | Lists lock history in your KeyVox account. |
| [List Lockers](actions/list-lockers.md) | GET | Lists lockers in your KeyVox account. |
| [List Locks](actions/list-locks.md) | GET | Lists locks in your KeyVox account. |
| [Set Lock State](actions/set-lock-state.md) | PUT | Sets a lock to locked or unlocked in KeyVox. |
| [Unlock Locker](actions/unlock-locker.md) | PUT | Unlocks an existing locker in KeyVox. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Place Details](actions/get-place-details.md) | GET | Retrieves place details from your KeyVox account. |
| [List Available Places](actions/list-available-places.md) | GET | Lists available places in your KeyVox account. |
| [List Places](actions/list-places.md) | GET | Lists places in your KeyVox account. |
| [List Reservable Units](actions/list-reservable-units.md) | GET | Lists doors in your KeyVox account. |
| [List Units](actions/list-units.md) | GET | Lists rooms and devices in your KeyVox account. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | DELETE | Cancels an existing booking in KeyVox. |
| [Check In Booking](actions/check-in-booking.md) | PUT | Checks a booking in to KeyVox. |
| [Check Out Booking](actions/check-out-booking.md) | PUT | Checks a booking out from KeyVox. |
| [Create Booking](actions/create-booking.md) | POST | Creates a new booking in KeyVox. |
| [Get Booking Details](actions/get-booking-details.md) | GET | Retrieves booking details from your KeyVox account. |
| [List Booking Orders](actions/list-booking-orders.md) | GET | Lists booking orders in your KeyVox account. |
| [List Bookings](actions/list-bookings.md) | GET | Lists bookings in your KeyVox account. |
| [Update Booking](actions/update-booking.md) | PUT | Updates an existing booking in KeyVox. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Plan Details](actions/get-plan-details.md) | GET | Retrieves room plan details from KeyVox. |
| [List Plans](actions/list-plans.md) | GET | Lists room plans in your KeyVox account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in KeyVox. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in KeyVox. |

