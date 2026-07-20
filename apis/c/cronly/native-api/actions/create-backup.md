# Create Backup with Cronly

## Endpoint

- **Method:** `POST`
- **Path:** `/api/backups`
- **Base URL:** `https://cronly.app`
- **Official documentation:** [Create Backup](https://docs.cronly.app/api/back-ups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | The username on the server whose backup you want to create. |
| `server_id` | body | `string` | yes | The identifier string of the server for the backup. |
| `file_content` | body | `string` | yes | The content of the crontab file. |
