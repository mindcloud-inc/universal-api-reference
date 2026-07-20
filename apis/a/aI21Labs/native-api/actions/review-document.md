# Review Document with AI21 Labs

Creates a document review run in AI21 Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/maestro/runs`
- **Base URL:** `https://api.ai21.com/studio/v1`
- **Official documentation:** [Review Document](https://docs.ai21.com/reference/maestro-create-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The text or document content to review. |
| `budget` | body | `string` | no | AI21 reasoning budget such as low, medium, or high. Accepted values: `0`, `1`, `2`. |
