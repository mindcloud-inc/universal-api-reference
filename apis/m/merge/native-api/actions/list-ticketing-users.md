# List Ticketing Users with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ticketing/v1/users`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [List Ticketing Users](https://docs.merge.dev/ticketing/users/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
