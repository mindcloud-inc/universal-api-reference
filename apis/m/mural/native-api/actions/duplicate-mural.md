# Duplicate Mural with Mural

Creates a new mural in Mural by duplicating another mural.

## Endpoint

- **Method:** `POST`
- **Path:** `/murals/:muralId/duplicate`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Duplicate Mural](https://developers.mural.co/public/reference/duplicatemural)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `muralId` | path | `string` | yes |
| `roomId` | body | `number` | yes |
| `title` | body | `string` | yes |
| `folderId` | body | `string` | no |
| `infinite` | body | `boolean` | no |
