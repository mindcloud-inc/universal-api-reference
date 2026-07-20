# List HRIS Companies with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/hris/v1/companies`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List HRIS Companies](https://docs.merge.dev/hris/companies/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
