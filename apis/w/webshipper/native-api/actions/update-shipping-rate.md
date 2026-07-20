# Update Shipping Rate with Webshipper

Updates a shipping rate in Webshipper.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/shipping_rates/:id`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Update Shipping Rate](https://docs.webshipper.io/#shipping_rates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
