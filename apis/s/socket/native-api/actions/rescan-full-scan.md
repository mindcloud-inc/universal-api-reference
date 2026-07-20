# Rescan Full Scan with Socket

Rescans an existing full scan in Socket.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/full-scans/:full_scan_id/rescan`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Rescan Full Scan](https://docs.socket.dev/reference/rescanorgfullscan)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `full_scan_id` | path | `string` | yes |
