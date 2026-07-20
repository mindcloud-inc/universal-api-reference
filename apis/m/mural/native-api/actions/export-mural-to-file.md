# Export Mural to File with Mural

Creates a new mural export in Mural.

## Endpoint

- **Method:** `POST`
- **Path:** `/murals/:muralId/export`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Export Mural to File](https://developers.mural.co/public/reference/exportmural)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `muralId` | path | `string` | yes |
| `downloadFormat` | body | `string` | yes |
