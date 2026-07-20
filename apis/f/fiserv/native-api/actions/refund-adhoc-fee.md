# Refund Adhoc Fee with Fiserv

Creates a refund for an adhoc fee in Fiserv.

## Endpoint

- **Method:** `POST`
- **Path:** `/fees/:id/refund`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Refund Adhoc Fee](https://isvportal.fiserv.com/docs/payments-api#operation/createRefund)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Fee ID to refund. |
| `amount` | body | `number` | yes | Refund amount in minor units. |
| `description` | body | `string` | yes | Refund description. |
| `reference_id` | body | `string` | no | Optional external reference ID. |
