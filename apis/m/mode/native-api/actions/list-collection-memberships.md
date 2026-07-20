# List Collection Memberships with Mode

List memberships for a specific collection in a Mode workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/[:space]/memberships`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [List Collection Memberships](https://mode.com/developer/api-reference/management/space-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Mode collection token. |
