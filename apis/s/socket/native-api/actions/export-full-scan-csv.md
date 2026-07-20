# Export Full Scan CSV with Socket

Exports full scan alerts from Socket as CSV.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/full-scans/:full_scan_id/format/csv`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Export Full Scan CSV](https://docs.socket.dev/reference/getorgfullscancsv)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `full_scan_id` | path | `string` | yes |
