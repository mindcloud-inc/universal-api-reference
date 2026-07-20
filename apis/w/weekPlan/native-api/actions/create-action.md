# Create Action with Week Plan

## Endpoint

- **Method:** `POST`
- **Path:** `actions`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Create Action](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Date` | body | `string` | no | Optional target date in YYYY-MM-DD format. |
| `Quadrant` | body | `number` | no | Optional Eisenhower quadrant for the new action. |
| `RoleId` | body | `number` | no | Optional role assignment for the new action. |
| `Text` | body | `string` | yes | Task text, including any Week Plan markdown prefixes such as #. |
| `WorkspaceId` | body | `number` | no | Optional workspace override for the new action. |
