# Create Note with HackMD

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://api.hackmd.io/v1`
- **Official documentation:** [Create Note](https://api.hackmd.io/v1/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | no |
| `content` | body | `string` | no |
| `description` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
| `readPermission` | body | `string` | no |
| `writePermission` | body | `string` | no |
| `parentFolderId` | body | `string` | no |
| `permalink` | body | `string` | no |
