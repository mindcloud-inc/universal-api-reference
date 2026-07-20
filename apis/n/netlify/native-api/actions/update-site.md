# Update Site with Netlify

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sites/:site_id`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Update Site](https://open-api.netlify.com/#operation/updateSite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | The Netlify site ID. |
| `name` | body | `string` | yes | The site name. |
