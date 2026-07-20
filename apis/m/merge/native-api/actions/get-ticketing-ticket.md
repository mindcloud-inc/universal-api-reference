# Get Ticketing Ticket with Merge

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ticketing/v1/tickets/{id}`
- **Base URL:** `https://api.merge.dev`
- **Official documentation:** [Get Ticketing Ticket](https://docs.merge.dev/ticketing/tickets/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountToken` | query | `string` | yes | Linked account token for the Merge account you want to query. The shared headers mapper sends this input as X-Account-Token. |
| `id` | path | `string` | yes | Merge object ID. |
