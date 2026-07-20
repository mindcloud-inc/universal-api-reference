# Get Page By ID (Fetch) with Agility CMS

Retrieves a published page by ID from Agility CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/:guid/fetch/:locale/page/:id`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Page By ID (Fetch)](https://api.aglty.io/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The pageID of the page to retrieve. |
