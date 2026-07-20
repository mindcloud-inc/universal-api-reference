# Update Action with Week Plan

## Endpoint

- **Method:** `POST`
- **Path:** `actions/full_patch`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Update Action](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ActionId` | body | `number` | yes | The action to update. |
| `Date` | body | `string` | no | Optional updated date in YYYY-MM-DD format. |
| `Quadrant` | body | `number` | no | Optional updated Eisenhower quadrant. |
| `RoleId` | body | `number` | no | Optional updated role assignment. |
| `Text` | body | `string` | no | Updated task text. |
| `WorkspaceId` | body | `number` | no | Optional workspace override while updating an action. |
