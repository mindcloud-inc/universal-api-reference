# Get Payment Method with Fiserv

Retrieves a payment method from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment_methods/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Get Payment Method](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment method id from the path. |
