# Cancel Charge with Reepay

Cancels a charge in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/charge/:handle/cancel`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Cancel Charge](https://docs.frisbii.com/reference/cancelcharge)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Charge handle from Reepay. |
