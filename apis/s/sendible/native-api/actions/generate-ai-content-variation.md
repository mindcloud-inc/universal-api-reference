# Generate AI Content Variation with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `1.0/api/ai/content`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Generate AI Content Variation](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `option` | query | `string` | yes | Transformation option such as rephrase. |
| `prompt` | query | `string` | yes | Prompt text to transform or rephrase. |
| `sessionId` | query | `string` | yes | AI session identifier. |
| `socialNetwork` | query | `string` | no | Optional social network when rephrasing for a specific channel. |
| `targetAudience` | query | `string` | no | Optional audience hint. |
| `tone` | query | `string` | no | Optional tone hint. |
