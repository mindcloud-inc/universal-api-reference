# Run Assistant with Griptape

Runs an assistant in Griptape.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/assistants/:assistant_id/runs`
- **Base URL:** `https://cloud.griptape.ai`
- **Official documentation:** [Run Assistant](https://docs.griptape.ai/stable/griptape-cloud/assistants/assistant-runs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | path | `string` | yes | The Griptape assistant ID to run. |
| `input` | body | `string` | no | Optional user input for the assistant run. |
| `thread_id` | body | `string` | no | Optional thread ID to attach the run to. |
| `stream` | body | `boolean` | no | Whether to return a live streamed Assistant Run response. |
| `ruleset_ids[]` | body | `array<string>` | no | Optional Ruleset IDs to attach to this Assistant Run. |
| `knowledge_base_ids[]` | body | `array<string>` | no | Optional Knowledge Base IDs to attach to this Assistant Run. |
| `structure_ids[]` | body | `array<string>` | no | Optional Structure IDs to attach to this Assistant Run. |
| `tool_ids[]` | body | `array<string>` | no | Optional Tool IDs to attach to this Assistant Run. |
