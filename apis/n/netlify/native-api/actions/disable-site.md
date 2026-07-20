# Disable Site with Netlify

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/disable`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Disable Site](https://open-api.netlify.com/#operation/disableSite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes | The Netlify site ID. |
| `reason` | query | `string` | yes | Reason for disabling the site. |
