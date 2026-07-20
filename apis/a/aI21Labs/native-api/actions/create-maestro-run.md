# Create Maestro Run with AI21 Labs

Creates a generic Maestro run in AI21 Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/maestro/runs`
- **Base URL:** `https://api.ai21.com/studio/v1`
- **Official documentation:** [Create Maestro Run](https://docs.ai21.com/reference/maestro-create-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The task, question, or source text to send to AI21 Maestro. |
| `budget` | body | `string` | no | AI21 reasoning budget such as low, medium, or high. Accepted values: `0`, `1`, `2`. |
| `system_prompt` | body | `string` | no | Optional system instructions that further guide the generic Maestro run. |
