# Delete Site Build Hook with Netlify

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sites/:site_id/build_hooks/:id`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Delete Site Build Hook](https://open-api.netlify.com/#operation/deleteSiteBuildHook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `string` | yes |
| `id` | path | `string` | yes |
