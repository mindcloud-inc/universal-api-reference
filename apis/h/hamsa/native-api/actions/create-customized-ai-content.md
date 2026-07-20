# Create Customized AI Content with Hamsa

Creates customized AI content in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/jobs/ai-content/custom`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Create Customized AI Content](https://docs.tryhamsa.com/api-reference/endpoint/create-customized-ai-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aiParts[]` | body | `array<object>` | yes | Send multiple values as a array. |
| `aiParts[]` | body | `array<object>` | yes | — |
| `aiParts[].aiPart` | body | `string` | yes | — |
| `aiParts[].aiPart` | body | `string` | yes | — |
| `aiParts[].language` | body | `string` | yes | — |
| `aiParts[].language` | body | `string` | yes | — |
| `aiParts[].prompt` | body | `string` | yes | — |
| `aiParts[].prompt` | body | `string` | yes | — |
| `jobId` | query | `string` | yes | — |
| `webhookAuth` | body | `object` | no | — |
| `webhookUrl` | body | `string` | no | — |
