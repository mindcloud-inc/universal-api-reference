# Update Order with Webshipper

Updates an order in Webshipper.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/orders/:id`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Update Order](https://docs.webshipper.io/#orders)

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
