# Get PACER NCL All Courts Results with Court Drive

## Endpoint

- **Method:** `GET`
- **Path:** `/pacer/ncl/all/{search_id}`
- **Base URL:** `https://v1.courtapi.com`
- **Official documentation:** [Get PACER NCL All Courts Results](https://www.courtapi.com/docs/playground)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_no` | query | `string` | yes | Result page number to retrieve. |
| `search_id` | path | `string` | yes | National case locator search identifier. |
