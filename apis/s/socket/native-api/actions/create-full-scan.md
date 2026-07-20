# Create Full Scan with Socket

Creates a new full scan in Socket.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/full-scans`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Create Full Scan](https://docs.socket.dev/reference/createorgfullscan)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch` | query | `string` | no |
| `commit_hash` | query | `string` | no |
| `commit_message` | query | `string` | no |
| `committers` | query | `string` | no |
| `integration_org_slug` | query | `string` | no |
| `integration_type` | query | `string` | no |
| `make_default_branch` | query | `boolean` | no |
| `pull_request` | query | `number` | no |
| `repo` | query | `string` | yes |
| `scan_type` | query | `string` | no |
| `set_as_pending_head` | query | `boolean` | no |
| `tmp` | query | `boolean` | no |
| `workspace` | query | `string` | no |
