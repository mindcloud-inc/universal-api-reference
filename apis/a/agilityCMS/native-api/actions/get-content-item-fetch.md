# Get Content Item (Fetch) with Agility CMS

Retrieves a published content item from Agility CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/:guid/fetch/:locale/item/:id`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Content Item (Fetch)](https://api.aglty.io/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The contentID of the item to retrieve. |
