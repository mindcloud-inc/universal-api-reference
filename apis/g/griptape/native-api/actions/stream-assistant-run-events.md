# Stream Assistant Run Events with Griptape

Streams assistant run events from Griptape.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/assistant-runs/:assistant_run_id/events/stream`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Stream Assistant Run Events](https://docs.griptape.ai/stable/griptape-cloud/assistants/assistant-runs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_run_id` | path | `string` | yes | The assistant run ID whose events should be streamed. |
