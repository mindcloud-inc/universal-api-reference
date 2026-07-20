# List Resources with Bokun

Retrieves resources and capacity details from Bokun.

## Endpoint

- **Method:** `GET`
- **Path:** `/restapi/v2.0/resources`
- **Base URL:** `https://api.bokun.io`
- **Official documentation:** [List Resources](https://api-docs.bokun.dev/rest-v2.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNo` | query | `number` | yes | The page number to fetch. |
| `pageSize` | query | `number` | yes | The number of records to fetch per page. |
