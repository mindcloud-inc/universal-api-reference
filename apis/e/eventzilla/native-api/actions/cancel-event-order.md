# Cancel Event Order with Eventzilla

Cancels an event order in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/order/cancel`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Cancel Event Order](https://developer.eventzilla.net/docs/#ev_orderCAN)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout_id` | body | `number` | yes | The checkout identifier to cancel. |
| `eventid` | body | `number` | yes | The Eventzilla event identifier. |
| `comments` | body | `string` | yes | Organizer comment to store with the cancellation. |
