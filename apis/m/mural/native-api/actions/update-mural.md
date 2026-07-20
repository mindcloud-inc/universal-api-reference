# Update Mural with Mural

Updates an existing mural in Mural.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/murals/:muralId`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Update Mural](https://developers.mural.co/public/reference/updatemuralbyid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `muralId` | path | `string` | yes |
| `title` | body | `string` | no |
| `folderId` | body | `string` | no |
| `width` | body | `number` | no |
| `height` | body | `number` | no |
| `infinite` | body | `boolean` | no |
| `favorite` | body | `boolean` | no |
| `status` | body | `string` | no |
