# Calculate Surcharge with Fiserv

Calculates a surcharge for a payment in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/surcharge`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Calculate Surcharge](https://isvportal.fiserv.com/docs/payments-api#operation/calculate_surcharge)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | query | `string` | yes | Merchant account ID required in the x-account-id header. |
| `payment_method_id` | body | `string` | yes | Payment method ID used to calculate the surcharge. |
| `postal_code` | body | `string` | no | Postal code for the surcharge calculation. |
| `amount` | body | `number` | yes | Payment amount in minor units. |
| `percent` | body | `number` | yes | Surcharge percentage, from 0 to 3. |
