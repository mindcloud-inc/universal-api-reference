# Get Page By Path (Fetch) with Agility CMS

Retrieves a published page by path from Agility CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/:guid/fetch/:locale/page/:channel`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Page By Path (Fetch)](https://api.aglty.io/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | The page path to resolve, for example /home or /blog. |
