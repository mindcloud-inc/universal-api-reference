# Validate Biller with Dataway

Validates a biller in Dataway for a selected service.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate-biller`
- **Base URL:** `https://datawayapp.com/vendor`
- **Official documentation:** [Validate Biller](https://documenter.getpostman.com/view/421216/UV5Ukz4U)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_slug` | body | `string` | yes | Vendor service slug to validate against. |
| `biller_identifier` | body | `string` | yes | Customer identifier such as phone number or meter number. |
| `variation_slug` | body | `string` | no | Optional variation slug when the service requires a variation. |
