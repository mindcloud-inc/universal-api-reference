# List Full Scans with Socket

Retrieves organization full scans from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/full-scans`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [List Full Scans](https://docs.socket.dev/reference/getorgfullscanlist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch` | query | `string` | no |
| `commit_hash` | query | `string` | no |
| `direction` | query | `string` | no |
| `from` | query | `date` | no |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `pull_request` | query | `number` | no |
| `repo` | query | `string` | no |
| `sort` | query | `string` | no |
| `use_cursor` | query | `boolean` | no |
| `workspace` | query | `string` | no |
