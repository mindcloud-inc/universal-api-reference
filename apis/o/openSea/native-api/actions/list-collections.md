# Get Multiple Collections with OpenSea

Retrieves collections from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/collections`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Multiple Collections](https://docs.opensea.io/reference/list_collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of collections to return per page |
| `next.value` | query | `string` | no | — |
| `chain` | query | `string` | no | Blockchain to filter by |
| `creator_username` | query | `string` | no | Username of collection creator to filter by |
| `include_hidden` | query | `boolean` | no | Include hidden collections in results |
| `order_by` | query | `string` | no | Field to order results by |
