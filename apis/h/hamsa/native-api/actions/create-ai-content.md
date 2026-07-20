# Create AI Content with Hamsa

Creates AI content in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/jobs/ai-content`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Create AI Content](https://docs.tryhamsa.com/api-reference/endpoint/create-ai-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aiParts[]` | body | `array<string>` | yes | Send multiple values as a array. |
| `jobId` | query | `string` | yes | — |
| `webhookAuth` | body | `string` | no | — |
| `webhookUrl` | body | `string` | no | — |
