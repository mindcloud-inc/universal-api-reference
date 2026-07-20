# Update Branch with Xano

Updates an existing branch in Xano.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api%3Ameta/workspace/:workspace_id/branch/:branch_label`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Update Branch](https://docs.xano.com/xano-features/metadata-api/instance_api/update_an_existing_branchs_label_description_or_color)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch_label` | path | `string` | yes |
| `workspace_id` | path | `number` | yes |
