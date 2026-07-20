# Create Mural with Mural

Creates a new mural in Mural.

## Endpoint

- **Method:** `POST`
- **Path:** `/murals`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Create Mural](https://developers.mural.co/public/reference/createmural)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `roomId` | body | `number` | yes |
| `title` | body | `string` | no |
| `folderId` | body | `string` | no |
| `width` | body | `number` | no |
| `height` | body | `number` | no |
| `infinite` | body | `boolean` | no |
