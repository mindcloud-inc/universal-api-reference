# List Fees with Fiserv

Retrieves fees for a merchant account from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/fees`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Fees](https://isvportal.fiserv.com/docs/payments-api#operation/getManyFees)

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
| `source_id` | query | `string` | no | Filter fees by source ID. |
| `starting_after` | query | `string` | no | Cursor ID to start after. |
| `x-account-id` | query | `string` | yes | Merchant account ID required in the x-account-id header. |
| `limit` | query | `number` | no | Maximum number of fees to return. |
| `fee_type` | query | `list` | no | Filter by fee type. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
