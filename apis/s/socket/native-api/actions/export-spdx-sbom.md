# Export SPDX SBOM with Socket

Exports a Socket SBOM in SPDX format.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/export/spdx/:id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Export SPDX SBOM](https://docs.socket.dev/reference/exportspdx)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
