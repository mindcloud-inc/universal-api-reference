# Create Room with Mural

Creates a new room in Mural.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms`
- **Base URL:** `https://app.mural.co/api/public/v1`
- **Official documentation:** [Create Room](https://developers.mural.co/public/reference/createroom)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | body | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
| `description` | body | `string` | no |
| `confidential` | body | `boolean` | no |
