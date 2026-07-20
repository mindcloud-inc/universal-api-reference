# List Prompt Versions with Arize AX

Retrieves versions for a prompt in Arize AX.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/prompts/:promptId/versions`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [List Prompt Versions](https://arize.com/docs/api-reference/prompts/list-prompt-versions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt_id` | path | `string` | yes |
