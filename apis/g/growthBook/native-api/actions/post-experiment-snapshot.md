# Create Experiment Snapshot with GrowthBook

Creates an experiment snapshot in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiments/:id/snapshot`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create Experiment Snapshot](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The experiment id of the experiment to update |
| `triggeredBy` | body | `string` | no | Set to "schedule" if you want this request to trigger notifications and other events as it if were a scheduled update. Defaults to manual. |
