# Update Project with Teamdeck

Updates an existing project in Teamdeck.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:id`
- **Base URL:** `https://api.teamdeck.io/v1`
- **Official documentation:** [Update Project](https://teamdeck.io/developers/api#operation/updateProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Teamdeck project ID. |
| `name` | body | `string` | yes | — |
| `color` | body | `string` | no | — |
| `archived` | body | `boolean` | no | — |
| `enable_time_entry_approval` | body | `boolean` | no | — |
| `default_approver_id` | body | `number` | no | — |
| `organization_unit_id` | body | `number` | no | — |
