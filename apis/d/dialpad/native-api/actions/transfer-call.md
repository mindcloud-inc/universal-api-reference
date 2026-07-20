# Transfer Call with Dialpad

Transfers a call to another recipient in Dialpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/call/:id/transfer`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Transfer Call](https://developers.dialpad.com/reference/calltransfer_call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The call's id. |
| `to` | body | `object` | no | Destination of the call transfer. |
| `transfer_state` | body | `string` | no | The state which the call should take when it's transferred. |
| `custom_data` | body | `string` | no | Extra data to associate with the call. |
