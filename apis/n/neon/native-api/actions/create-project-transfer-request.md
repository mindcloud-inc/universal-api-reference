# Create a project transfer request with Neon

Creates a project transfer request in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/transfer_requests`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create a project transfer request](https://api-docs.neon.tech/reference/createprojecttransferrequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `ttl_seconds` | body | `number` | no | Neon API parameter ttl_seconds |
