# Get Content Item V1 (Preview) with Agility CMS

Retrieves a preview content item from Agility CMS v1.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:guid/preview/:locale/item/:id`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Content Item V1 (Preview)](https://api.aglty.io/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The contentID of the item to retrieve. |
