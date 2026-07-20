# Delete Block List Numbers with Phonely

Deletes phone numbers from the Phonely block list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/agent-block-list`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Delete Block List Numbers](https://docs.phonely.ai/api-reference/endpoint/block-list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uid` | body | `string` | yes |
| `agentId` | body | `string` | yes |
| `numbers[]` | body | `array<string>` | yes |
