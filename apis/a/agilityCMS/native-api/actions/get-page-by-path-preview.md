# Get Page By Path (Preview) with Agility CMS

Retrieves a preview page by path from Agility CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/:guid/preview/:locale/page/:channel`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [Get Page By Path (Preview)](https://api.aglty.io/swagger/v2/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | The page path to resolve, for example /home or /blog. |
