# Enable Site with Netlify

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/enable`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Enable Site](https://open-api.netlify.com/#operation/enableSite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | The Netlify site ID. |
