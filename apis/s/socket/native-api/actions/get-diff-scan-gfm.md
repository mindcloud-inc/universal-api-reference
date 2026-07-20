# Get Diff Scan GFM with Socket

Retrieves a diff scan as GitHub Flavored Markdown from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/diff-scans/:diff_scan_id/gfm`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Get Diff Scan GFM](https://docs.socket.dev/reference/getdiffscangfm)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `diff_scan_id` | path | `string` | yes |
