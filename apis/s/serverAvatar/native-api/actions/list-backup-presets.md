# List Backup Presets with ServerAvatar

Retrieves backup presets from ServerAvatar.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{{organization}}/servers/{{server}}/backups/presets`
- **Base URL:** `https://api.serveravatar.com`
- **Official documentation:** [List Backup Presets](https://serveravatar.com/api-docs/endpoint/backup/preset.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | path | `string` | yes |
| `server` | path | `string` | yes |
