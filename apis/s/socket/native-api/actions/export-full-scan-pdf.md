# Export Full Scan PDF with Socket

Exports full scan alerts from Socket as PDF.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/full-scans/:full_scan_id/format/pdf`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Export Full Scan PDF](https://docs.socket.dev/reference/getorgfullscanpdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `full_scan_id` | path | `string` | yes |
