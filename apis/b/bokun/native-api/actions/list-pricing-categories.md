# List Pricing Categories with Bokun

Retrieves pricing categories from the current Bokun vendor.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/pricing/categories`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [List Pricing Categories](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNo` | query | `number` | yes | The page number to fetch. |
| `pageSize` | query | `number` | yes | The number of records to fetch per page. |
