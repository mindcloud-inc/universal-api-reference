# Get Ticketing User with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ticketing/v1/users/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get Ticketing User](https://docs.merge.dev/ticketing/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |
