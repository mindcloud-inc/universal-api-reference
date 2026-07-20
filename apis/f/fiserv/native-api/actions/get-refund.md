# Get Refund with Fiserv

Retrieves detailed refund information from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/refunds/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Refund](https://isvportal.fiserv.com/docs/payments-api#operation/get_refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Refund id from the path. |
