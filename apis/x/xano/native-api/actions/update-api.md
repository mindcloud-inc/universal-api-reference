# Update API with Xano

Updates an existing API endpoint in Xano.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Update API](https://docs.xano.com/xano-features/metadata-api/instance_api/update_api_endpoint_code_settings_and_authentication_rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_id` | path | `number` | yes | The Xano API ID. |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `description` | body | `string` | yes | API endpoint description. |
| `name` | body | `string` | yes | API endpoint name. |
| `verb` | body | `string` | yes | HTTP verb for the endpoint. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
