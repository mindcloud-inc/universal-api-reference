# Search Site Functions with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/functions`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Search Site Functions](https://open-api.netlify.com/#operation/searchSiteFunctions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | The Netlify site ID. |
| `filter` | query | `string` | no | Filter functions for the site. |
