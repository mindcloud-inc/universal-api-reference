# Create Custom Vocabulary with Rev AI

Creates a custom vocabulary in Rev AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/speechtotext/v1/vocabularies`
- **Base URL:** `https://api.rev.ai`
- **Official documentation:** [Create Custom Vocabulary](https://docs.rev.ai/api/custom-vocabulary/reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_vocabularies[]` | body | `array<object>` | yes |
| `metadata` | body | `string` | no |
| `strict` | body | `boolean` | no |
