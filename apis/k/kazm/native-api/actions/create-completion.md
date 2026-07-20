# Create Completion with Kazm

Creates a completion in Kazm.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/completions`
- **Base URL:** `https://api.lightningrod.ai/api/public/v1`
- **Official documentation:** [Create Completion](https://docs.lightningrod.ai/rest-api/transform-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Model identifier to use for the completion. |
| `prompt` | body | `string` | no | Prompt to complete. |
