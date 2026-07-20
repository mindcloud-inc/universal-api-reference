# Update Room with Mural

Updates an existing room in Mural.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rooms/:roomId`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Update Room](https://developers.mural.co/public/reference/updateroombyid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `roomId` | path | `number` | yes |
| `name` | body | `string` | no |
| `type` | body | `string` | no |
| `description` | body | `string` | no |
| `favorite` | body | `boolean` | no |
