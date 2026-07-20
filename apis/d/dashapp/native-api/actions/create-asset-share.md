# Create Asset Share with Dash.app

Creates a new asset share in Dash.app.

## Endpoint

- **Method:** `POST`
- **Path:** `/asset-shares`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Create Asset Share](https://api-docs.dash.app/dash/openapi/asset-shares/createassetshare)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assetIds[]` | body | `array<string>` | yes |
| `assetPermittedActions` | body | `string` | no |
| `expiry` | body | `string` | yes |
