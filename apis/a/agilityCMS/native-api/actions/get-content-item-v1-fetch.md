# Get Content Item V1 (Fetch) with Agility CMS

Retrieves a published content item from Agility CMS v1.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:guid/fetch/:locale/item/:id`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Content Item V1 (Fetch)](https://api.aglty.io/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The contentID of the item to retrieve. |
