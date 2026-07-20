# KeyVox: Native API Reference

A consolidated summary of KeyVox's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.keyvox.co/
- **API base URL:** `https://eco.blockchainlock.io/api/eagle-pms`

## Authentication

### API Key

HMAC API key authentication using an API key and secret key.

### Credentials

- **API Key:** `apiKey` · required
- **Secret Key:** `secretKey` · required · The KeyVox secret key paired with your API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.keyvox.co/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | `POST /bacsorder/cancel` | [docs](https://developers.keyvox.co/) |
| [Check In Booking](actions/check-in-booking.md) | `POST /bacsorder/checkin` | [docs](https://developers.keyvox.co/) |
| [Check Out Booking](actions/check-out-booking.md) | `POST /bacsorder/checkout` | [docs](https://developers.keyvox.co/) |
| [Create Booking](actions/create-booking.md) | `POST /bacsorder/create` | [docs](https://developers.keyvox.co/) |
| [Create Lock Card](actions/create-lock-card.md) | `POST /v1/setCard` | [docs](https://developers.keyvox.co/) |
| [Create Lock PIN](actions/create-lock-pin.md) | `POST /v1/createLockPin` | [docs](https://developers.keyvox.co/) |
| [Create Locker PIN](actions/create-locker-pin.md) | `POST /v1/createLockerPin` | [docs](https://developers.keyvox.co/) |
| [Create User](actions/create-user.md) | `POST /v1/users` | [docs](https://developers.keyvox.co/) |
| [Delete Lock Card](actions/delete-lock-card.md) | `POST /v1/disableCard` | [docs](https://developers.keyvox.co/) |
| [Delete Lock PIN](actions/delete-lock-pin.md) | `POST /v1/disableLockPin` | [docs](https://developers.keyvox.co/) |
| [Delete Locker PIN](actions/delete-locker-pin.md) | `POST /v1/disableLockerPin` | [docs](https://developers.keyvox.co/) |
| [Get Booking Details](actions/get-booking-details.md) | `POST /bacsorder/detail` | [docs](https://developers.keyvox.co/) |
| [Get Lock Card Status](actions/get-lock-card-status.md) | `POST /v1/getCardStatus` | [docs](https://developers.keyvox.co/) |
| [Get Lock PIN Status](actions/get-lock-pin-status.md) | `POST /v1/getLockPinStatus` | [docs](https://developers.keyvox.co/) |
| [Get Lock Status](actions/get-lock-status.md) | `POST /v1/getLockStatus` | [docs](https://developers.keyvox.co/) |
| [Get Locker Status](actions/get-locker-status.md) | `POST /v1/getLockerStatus` | [docs](https://developers.keyvox.co/) |
| [Get Place Details](actions/get-place-details.md) | `POST /place/detail` | [docs](https://developers.keyvox.co/) |
| [Get Plan Details](actions/get-plan-details.md) | `POST /plan/detail` | [docs](https://developers.keyvox.co/) |
| [Issue Lock Key](actions/issue-lock-key.md) | `POST /v1/issueLockKey` | [docs](https://developers.keyvox.co/) |
| [List Available Places](actions/list-available-places.md) | `POST /place/availableList` | [docs](https://developers.keyvox.co/) |
| [List Booking Orders](actions/list-booking-orders.md) | `POST /v1/getBookingOrders` | [docs](https://developers.keyvox.co/) |
| [List Bookings](actions/list-bookings.md) | `POST /bacsorder/list` | [docs](https://developers.keyvox.co/) |
| [List Lock Cards](actions/list-lock-cards.md) | `POST /v1/getLockCardList` | [docs](https://developers.keyvox.co/) |
| [List Lock Events](actions/list-lock-events.md) | `POST /v1/locks/events` | [docs](https://developers.keyvox.co/) |
| [List Lock History](actions/list-lock-history.md) | `POST /v1/getLockHistory` | [docs](https://developers.keyvox.co/) |
| [List Lock PINs](actions/list-lock-pi-ns.md) | `POST /v1/getLockPinList` | [docs](https://developers.keyvox.co/) |
| [List Lockers](actions/list-lockers.md) | `POST /v1/getLockers` | [docs](https://developers.keyvox.co/) |
| [List Locks](actions/list-locks.md) | `POST /v1/getLocks` | [docs](https://developers.keyvox.co/) |
| [List Places](actions/list-places.md) | `POST /place/list` | [docs](https://developers.keyvox.co/) |
| [List Plans](actions/list-plans.md) | `POST /plan/list` | [docs](https://developers.keyvox.co/) |
| [List Reservable Units](actions/list-reservable-units.md) | `POST /unit/list` | [docs](https://developers.keyvox.co/) |
| [List Unit PINs](actions/list-unit-pi-ns.md) | `POST /v1/getUnitPinList` | [docs](https://developers.keyvox.co/) |
| [List Units](actions/list-units.md) | `POST /v1/getUnits` | [docs](https://developers.keyvox.co/) |
| [Set Lock State](actions/set-lock-state.md) | `POST /v1/unlock` | [docs](https://developers.keyvox.co/) |
| [Unlock Locker](actions/unlock-locker.md) | `POST /v1/unlockLocker` | [docs](https://developers.keyvox.co/) |
| [Update Booking](actions/update-booking.md) | `POST /bacsorder/update` | [docs](https://developers.keyvox.co/) |
| [Update Lock Card](actions/update-lock-card.md) | `POST /v1/updateCard` | [docs](https://developers.keyvox.co/) |
| [Update Lock PIN](actions/update-lock-pin.md) | `POST /v1/changeLockPin` | [docs](https://developers.keyvox.co/) |
| [Update Locker PIN](actions/update-locker-pin.md) | `POST /v1/changeLockerPin` | [docs](https://developers.keyvox.co/) |
| [Update User](actions/update-user.md) | `PUT /v1/users/{{userId}}` | [docs](https://developers.keyvox.co/) |
