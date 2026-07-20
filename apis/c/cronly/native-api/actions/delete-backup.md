# Delete Backup with Cronly

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/backups/:server_id/:username`
- **Base URL:** `https://cronly.app`
- **Official documentation:** [Delete Backup](https://docs.cronly.app/api/back-ups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | path | `string` | yes | The identifier string of the server whose backup you want to delete. |
| `username` | path | `string` | yes | The username on the server whose backup you want to delete. |
