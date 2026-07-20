# Export CycloneDX SBOM with Socket

Exports a Socket SBOM in CycloneDX format.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/export/cdx/:id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Export CycloneDX SBOM](https://docs.socket.dev/reference/exportcdx)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
