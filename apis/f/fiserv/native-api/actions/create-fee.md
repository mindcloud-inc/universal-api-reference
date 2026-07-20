# Create Fee with Fiserv

Creates a fee for a merchant account in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/fees`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Create Fee](https://isvportal.fiserv.com/docs/payments-api#operation/createFee)

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
| `fee_type` | body | `list` | yes | Fee type to create. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `amount` | body | `number` | yes | Fee amount in minor units. |
| `currency` | body | `list` | no | Currency for the fee. Accepted values: `0`, `1`. |
| `description` | body | `string` | yes | Fee description. |
| `reference_id` | body | `string` | no | Optional external reference ID. |
