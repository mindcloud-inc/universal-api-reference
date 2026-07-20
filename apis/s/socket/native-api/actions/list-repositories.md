# List Repositories with Socket

Retrieves organization repositories available in Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/repos`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [List Repositories](https://docs.socket.dev/reference/getorgrepolist)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `direction` | query | `string` | no |
| `include_archived` | query | `boolean` | no |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `sort` | query | `string` | no |
