# Update Asset Share with Dash.app

Updates an existing asset share in Dash.app.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/asset-shares/:id`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Update Asset Share](https://api-docs.dash.app/dash/openapi/asset-shares/patchassetshare)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assetPermittedActions` | body | `string` | no |
| `expiry` | body | `string` | no |
| `id` | path | `string` | yes |
