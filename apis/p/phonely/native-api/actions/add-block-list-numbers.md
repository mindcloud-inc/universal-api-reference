# Add Block List Numbers with Phonely

Adds phone numbers to the Phonely block list.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/agent-block-list`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Add Block List Numbers](https://docs.phonely.ai/api-reference/endpoint/block-list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uid` | body | `string` | yes |
| `agentId` | body | `string` | yes |
| `numbers[]` | body | `array<string>` | yes |
