# Update Payment Method with Fiserv

Updates an existing payment method in Fiserv.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/payment_methods/{id}`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Update Payment Method](https://isvportal.fiserv.com/docs/payments-api#operation/update_payment_method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment method id from the path. |
| `requestBody` | body | `object` | yes | JSON request body from the official update payment method schema. |
