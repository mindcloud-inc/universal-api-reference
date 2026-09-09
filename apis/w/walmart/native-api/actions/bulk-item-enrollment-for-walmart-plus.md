# Bulk Item Enrollment for Walmart+ with Walmart

Manage item participation in the Walmart+ program.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Item Enrollment for Walmart+](https://developer.walmart.com/us-marketplace/reference/post_v3-feeds)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `list<string>` | no | Allowed: `PROGRAM_ACTIONS` |
| `fileName` | body | `file` | no | — |
| `requestType` | query | `string` | no | `WALMART_PLUS_SFF` - Specifies the type of request for the Walmart+ SFF (Seller-Fulfilled) program. |
