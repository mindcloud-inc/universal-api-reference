# Create Site Build Hook with Netlify

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/build_hooks`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [Create Site Build Hook](https://open-api.netlify.com/#operation/createSiteBuildHook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site_id` | path | `list<string>` | yes |
| `title` | body | `string` | no |
| `branch` | body | `string` | no |
