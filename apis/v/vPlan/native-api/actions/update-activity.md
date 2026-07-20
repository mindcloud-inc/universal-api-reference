# Update Activity with vPlan

## Endpoint

- **Method:** `PUT`
- **Path:** `/activity/[:id]`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Update Activity](https://docs.api.vplan.com/activity.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | Activity description. |
| `id` | path | `string` | yes | Activity identifier. |
