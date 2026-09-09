# Bulk Item Setup (multiple) with Walmart

Set up a new seller fulfilled item.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Item Setup (multiple)](https://developer.walmart.com/us-marketplace/reference/itembulkuploads)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | no |
