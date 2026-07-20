# Update Media with Wistia

Updates an existing media item in Wistia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/modern/medias/:mediaHashedId`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Update Media](https://docs.wistia.com/reference/put_medias-mediahashedid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `mediaHashedId` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
