# Delete Diff Scan with Socket

Deletes an existing diff scan from Socket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orgs/:org_slug/diff-scans/:diff_scan_id`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Delete Diff Scan](https://docs.socket.dev/reference/deleteorgdiffscan)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `diff_scan_id` | path | `string` | yes |
