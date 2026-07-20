# Add Lead To Client Folder with noCRM.io

Adds a lead to a client folder in noCRM.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:id/add_to_client`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Add Lead To Client Folder](https://www.nocrm.io/api#add-a-lead-to-a-client-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lead ID. |
| `client_id` | body | `number` | yes | Client folder ID. |
