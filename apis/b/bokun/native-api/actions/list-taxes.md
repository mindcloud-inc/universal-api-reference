# List Taxes with Bokun

Retrieves taxes owned by the current Bokun vendor.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/taxes`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [List Taxes](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNo` | query | `number` | yes | The page number to fetch. |
| `pageSize` | query | `number` | yes | The number of records to fetch per page. |
