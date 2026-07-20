# Get PACER NCL Civil Results with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/pacer/ncl/civil/{search_id}`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Get PACER NCL Civil Results](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_no` | query | `string` | yes | Result page number to retrieve. |
| `search_id` | path | `string` | yes | National civil search identifier. |
