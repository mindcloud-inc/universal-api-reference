# List Group Memberships with Mode

List memberships for a specific group in a Mode workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/[:groupToken]/memberships`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [List Group Memberships](https://mode.com/developer/api-reference/management/group-memberships/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupToken` | path | `string` | yes | Mode group token. |
