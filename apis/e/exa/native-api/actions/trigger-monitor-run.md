# Trigger Monitor Run with Exa

Triggers a monitor run in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/monitors/:id/trigger`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Trigger Monitor Run](https://exa.ai/docs/reference/monitors-api-guide-for-coding-agents#post-/monitors/id/trigger-%E2%80%94-trigger-a-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Monitor identifier. |
