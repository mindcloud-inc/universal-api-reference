# Update Note with HackMD

## Endpoint

- **Method:** `PATCH`
- **Path:** `/notes/:noteId`
- **Base URL:** `https://api.hackmd.io/v1`
- **Official documentation:** [Update Note](https://api.hackmd.io/v1/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `noteId` | path | `string` | yes |
| `title` | body | `string` | no |
| `content` | body | `string` | no |
| `description` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
| `readPermission` | body | `string` | no |
| `writePermission` | body | `string` | no |
| `parentFolderId` | body | `string` | no |
| `permalink` | body | `string` | no |
