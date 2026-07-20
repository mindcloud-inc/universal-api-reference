# Trigger a job with Wisewand

Triggers a job in your Wisewand workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/jobs/:name`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [Trigger a job](https://api.wisewand.ai/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The job name (e.g., generate-image) |
