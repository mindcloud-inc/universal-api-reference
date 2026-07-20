# List HRIS Employees with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/hris/v1/employees`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List HRIS Employees](https://docs.merge.dev/hris/employees/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
