# Update Reservation Status with Restoplace

Updates a reservation status in Restoplace.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reserves/:id/status`
- **Base URL:** `https://api.restoplace.cc`
- **Official documentation:** [Update Reservation Status](https://restoplace.cc/help/API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique Restoplace reservation ID. |
| `status` | body | `number` | yes | Reservation status code. |
| `cancel_reason` | body | `number` | no | Cancel reason ID from the List Reservation Cancel Reasons action. |
| `cancel_reason_text` | body | `string` | no | Additional cancel reason text when required by the provider. |
