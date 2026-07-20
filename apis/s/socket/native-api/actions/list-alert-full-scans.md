# List Alert Full Scans with Socket

Retrieves full scans associated with alerts from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/alert-full-scan-search`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [List Alert Full Scans](https://docs.socket.dev/reference/alertfullscans)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `alertKey` | query | `string` | no |
| `per_page` | query | `string` | no |
| `range` | query | `string` | no |
| `startAfterCursor` | query | `string` | no |
