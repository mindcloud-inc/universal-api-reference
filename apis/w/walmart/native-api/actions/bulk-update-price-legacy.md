# Bulk Update Price ( Legacy ) with Walmart

Updates prices in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Update Price ( Legacy )](https://developer.walmart.com/us-marketplace/reference/pricebulkuploads#:~:text=Utilities-,Update%20Bulk%20Prices%20%28Multiple%29,-POST)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `feedType` | query | `list<string>` | yes |
| `file` | body | `file` | no |
