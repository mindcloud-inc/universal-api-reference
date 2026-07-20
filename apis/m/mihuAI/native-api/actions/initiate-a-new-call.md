# Initiate a New Call with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/call`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Initiate a New Call](https://developers.mihu.ai/api-reference/call/initiate-a-new-call)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | body | `string` | yes |
| `message.start` | body | `string` | no |
| `participant.about` | body | `string` | no |
| `participant.number` | body | `string` | yes |
| `prompt.content` | body | `string` | no |
| `prompt.overwrite` | body | `boolean` | yes |
