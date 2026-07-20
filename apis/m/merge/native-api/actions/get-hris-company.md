# Get HRIS Company with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/hris/v1/companies/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get HRIS Company](https://docs.merge.dev/hris/companies/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |
