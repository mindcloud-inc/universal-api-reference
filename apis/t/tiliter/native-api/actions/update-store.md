# Update Store with Tiliter

Updates a store in the Tiliter Recognition API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stores/:store_id`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Update Store](https://developer.tiliter.com/reference/update_store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `store_id` | path | `string` | yes | Store ID in the request path. |
| `storeId` | body | `string` | yes | Store ID in the request body. Must match Store ID Path. |
| `region` | body | `string` | yes | — |
| `friendlyName` | body | `string` | yes | — |
| `country` | body | `string` | yes | — |
| `areaCode` | body | `string` | yes | — |
