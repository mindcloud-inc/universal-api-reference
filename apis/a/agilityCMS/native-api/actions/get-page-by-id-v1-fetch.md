# Get Page By ID V1 (Fetch) with Agility CMS

Retrieves a published page by ID from Agility CMS v1.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:guid/fetch/:locale/page/:id`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Page By ID V1 (Fetch)](https://api.aglty.io/swagger/v1/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The pageID of the page to retrieve. |
