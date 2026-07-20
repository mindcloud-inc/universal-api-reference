# Confirm Event Order with Eventzilla

Confirms an event order in Eventzilla.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/order/confirm`
- **Base URL:** `https://www.eventzillaapi.net/api/v2`
- **Official documentation:** [Confirm Event Order](https://developer.eventzilla.net/docs/#ev_orderCNF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout_id` | body | `number` | yes | The checkout identifier to confirm. |
| `eventid` | body | `number` | yes | The Eventzilla event identifier. |
| `comments` | body | `string` | yes | Organizer comment to store with the confirmation. |
| `sendemail` | body | `boolean` | no | Set false to avoid sending the confirmation email. |
