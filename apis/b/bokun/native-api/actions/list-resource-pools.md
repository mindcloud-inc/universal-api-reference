# List Resource Pools with Bokun

Retrieves resource pool records from Bokun.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/resource/pools`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [List Resource Pools](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNo` | query | `number` | yes | The page number to fetch. |
| `pageSize` | query | `number` | yes | The number of records to fetch per page. |
