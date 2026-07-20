# List Diff Scans with Socket

Retrieves organization diff scans from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/diff-scans`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [List Diff Scans](https://docs.socket.dev/reference/listorgdiffscans)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `after_full_scan_id` | query | `string` | no |
| `before_full_scan_id` | query | `string` | no |
| `cursor` | query | `string` | no |
| `direction` | query | `string` | no |
| `per_page` | query | `number` | no |
| `repository_id` | query | `string` | no |
| `sort` | query | `string` | no |
