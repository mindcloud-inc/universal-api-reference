# Create Stage with vPlan

## Endpoint

- **Method:** `POST`
- **Path:** `/stage`
- **Base URL:** `https://api.vplan.com/v1`
- **Official documentation:** [Create Stage](https://docs.api.vplan.com/stage.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board_id` | body | `string` | yes | Board identifier for the new stage. |
| `delay_day` | body | `number` | yes | Stage delay day value. |
| `name` | body | `string` | yes | Stage name. |
| `priority` | body | `number` | yes | Stage priority. |
