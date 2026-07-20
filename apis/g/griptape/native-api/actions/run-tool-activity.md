# Run Tool Activity with Griptape

Runs a tool activity in Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tools/:tool_id/activities/:activity_name`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Run Tool Activity](https://docs.griptape.ai/stable/griptape-cloud/tools/run-tool/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activity_name` | path | `string` | yes | The activity name to invoke on the tool. |
| `tool_id` | path | `string` | yes | The Griptape tool ID to invoke. |
