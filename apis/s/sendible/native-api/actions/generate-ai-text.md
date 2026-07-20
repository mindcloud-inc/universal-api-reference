# Generate AI Text with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `1.0/api/ai/text_generation`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Generate AI Text](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | query | `string` | yes | Prompt text to generate from. |
| `sessionId` | query | `string` | yes | AI session identifier. |
| `targetAudience` | query | `string` | no | Optional audience hint. |
| `tone` | query | `string` | no | Optional tone hint. |
