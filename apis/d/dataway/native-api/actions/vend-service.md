# Vend Service with Dataway

Creates a new vend transaction in Dataway.

## Endpoint

- **Method:** `POST`
- **Path:** `/vend`
- **Base URL:** `https://datawayapp.com/vendor`
- **Official documentation:** [Vend Service](https://documenter.getpostman.com/view/421216/UV5Ukz4U)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_slug` | body | `string` | yes | Vendor service slug to vend. |
| `biller_identifier` | body | `string` | yes | Customer identifier such as phone number or smartcard number. |
| `variation_slug` | body | `string` | no | Optional variation slug when the service requires a variation. |
| `amount` | body | `string` | yes | Vend amount in naira when the service accepts arbitrary values. |
| `reference` | body | `string` | yes | Unique client reference for the vend request. |
