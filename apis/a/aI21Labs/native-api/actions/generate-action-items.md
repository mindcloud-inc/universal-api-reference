# Generate Action Items with AI21 Labs

Creates an action item extraction run in AI21 Labs.

## Endpoint

- **Method:** `POST`
- **Path:** `/maestro/runs`
- **Base URL:** `https://api.ai21.com/studio/v1`
- **Official documentation:** [Generate Action Items](https://docs.ai21.com/reference/maestro-create-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | The source content to analyze for action items. |
| `budget` | body | `string` | no | AI21 reasoning budget such as low, medium, or high. Accepted values: `0`, `1`, `2`. |
