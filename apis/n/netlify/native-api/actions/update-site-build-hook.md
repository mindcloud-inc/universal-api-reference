# Update Site Build Hook with Netlify

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/build_hooks/:id`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Update Site Build Hook](https://open-api.netlify.com/#operation/updateSiteBuildHook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `string` | yes |
| `id` | path | `string` | yes |
| `title` | body | `string` | no |
| `branch` | body | `string` | no |
