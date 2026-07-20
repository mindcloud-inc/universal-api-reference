# Get Backup with Cronly

## Endpoint

- **Method:** `GET`
- **Path:** `/api/backups/:server_id/:username`
- **Base URL:** `https://cronly.app`
- **Official documentation:** [Get Backup](https://docs.cronly.app/api/back-ups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | path | `string` | yes | The identifier string of the server for the backup. |
| `username` | path | `string` | yes | The username on the server whose backup you want to view. |
