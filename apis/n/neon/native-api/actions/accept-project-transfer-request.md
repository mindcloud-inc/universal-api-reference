# Accept a project transfer request with Neon

Accepts a project transfer request in Neon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/transfer_requests/:request_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Accept a project transfer request](https://api-docs.neon.tech/reference/acceptprojecttransferrequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `request_id` | path | `string` | yes | Neon API parameter request_id |
| `org_id` | body | `string` | no | Neon API parameter org_id |
