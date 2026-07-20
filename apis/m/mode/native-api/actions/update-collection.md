# Update Collection with Mode

Update a collection in a Mode workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/spaces/[:space]`
- **Base URL:** `https://app.mode.com/api/{workspace}`
- **Official documentation:** [Update Collection](https://mode.com/developer/api-reference/management/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space` | path | `string` | yes | Mode collection token. |
| `space` | body | `object` | yes | Collection fields to update. |
