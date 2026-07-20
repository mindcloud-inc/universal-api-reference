# Create Diff Scan from IDs with Socket

Creates a diff scan in Socket from scan IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/diff-scans/from-ids`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Create Diff Scan from IDs](https://docs.socket.dev/reference/createorgdiffscanfromids)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `before` | query | `string` | yes |
| `external_href` | query | `string` | no |
| `after` | query | `string` | yes |
| `description` | query | `string` | no |
| `merge` | query | `boolean` | no |
