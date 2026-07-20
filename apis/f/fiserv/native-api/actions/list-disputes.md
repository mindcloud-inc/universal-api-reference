# List Disputes with Fiserv

Retrieves disputes and dispute details from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/disputes`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Disputes](https://isvportal.fiserv.com/docs/payments-api#operation/get_disputes)

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
| `status` | query | `list` | no | Dispute status filter. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `limit` | query | `number` | no | Maximum number of disputes to return. Official max is 50. |
