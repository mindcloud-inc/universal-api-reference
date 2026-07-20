# Delete Alert Triage with Socket

Deletes an existing alert triage rule from Socket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orgs/:org_slug/triage/alerts/:uuid`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Delete Alert Triage](https://docs.socket.dev/reference/deleteorgalerttriage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uuid` | path | `string` | yes |
