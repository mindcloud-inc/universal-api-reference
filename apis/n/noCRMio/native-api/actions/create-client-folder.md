# Create Client Folder with noCRM.io

Creates a new client folder in noCRM.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Create Client Folder](https://www.nocrm.io/api#create-a-client-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Client folder name. |
| `description` | body | `string` | no | Client folder description. |
| `user_id` | body | `string` | no | User email or ID to assign the folder to. |
