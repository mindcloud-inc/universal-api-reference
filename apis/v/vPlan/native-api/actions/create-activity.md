# Create Activity with vPlan

## Endpoint

- **Method:** `POST`
- **Path:** `/activity`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Create Activity](https://docs.api.vplan.com/activity.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | body | `string` | yes | Board identifier for the new activity. |
| `description` | body | `string` | yes | Activity description. |
| `name` | body | `string` | yes | Activity name. |
