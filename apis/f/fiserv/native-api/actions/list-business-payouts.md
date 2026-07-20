# List Business Payouts with Fiserv

Retrieves payouts for a business from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/payouts`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Business Payouts](https://isvportal.fiserv.com/docs/payments-api#operation/get_payouts_by_business)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ending_before` | query | `string` | no | Cursor ID to end before. |
| `starting_after` | query | `string` | no | Cursor ID to start after. |
| `x-business-id` | query | `string` | yes | Business ID required in the x-business-id header. |
| `limit` | query | `number` | no | Maximum number of business payouts to return. Official max is 50. |
