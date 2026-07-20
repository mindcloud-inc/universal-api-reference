# Transfer projects between organizations with Neon

Transfers projects between organizations in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:source_org_id/projects/transfer`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Transfer projects between organizations](https://api-docs.neon.tech/reference/transferprojectsfromorgtoorg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_org_id` | path | `string` | yes | Neon API parameter source_org_id |
| `destination_org_id` | body | `string` | yes | Neon API parameter destination_org_id |
| `project_ids[]` | body | `array<string>` | yes | Neon API parameter project_ids |
