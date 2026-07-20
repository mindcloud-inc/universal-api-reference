# Stream Full Scan with Socket

Streams full scan artifacts from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/full-scans/:full_scan_id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Stream Full Scan](https://docs.socket.dev/reference/getorgfullscan)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cached` | query | `boolean` | no |
| `include_alert_priority_details` | query | `boolean` | no |
| `full_scan_id` | path | `string` | yes |
| `include_license_details` | query | `boolean` | yes |
