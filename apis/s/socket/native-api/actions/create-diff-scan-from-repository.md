# Create Diff Scan from Repository with Socket

Creates a diff scan in Socket from a repository.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/diff-scans/from-repo/:repo_slug`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Create Diff Scan from Repository](https://docs.socket.dev/reference/createorgrepodiff)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch` | query | `string` | no |
| `commit_hash` | query | `string` | no |
| `commit_message` | query | `string` | no |
| `committers` | query | `list<string>` | no |
| `description` | query | `string` | no |
| `external_href` | query | `string` | no |
| `integration_org_slug` | query | `string` | no |
| `integration_type` | query | `string` | no |
| `merge` | query | `boolean` | no |
| `pull_request` | query | `number` | no |
| `workspace` | query | `string` | no |
| `repo_slug` | path | `string` | yes |
