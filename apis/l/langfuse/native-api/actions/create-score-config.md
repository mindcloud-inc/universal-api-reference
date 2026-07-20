# Create Score Config with Langfuse

Creates a score config in Langfuse.

## Endpoint

- **Method:** `POST`
- **Path:** `/score-configs`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Create Score Config](https://api.reference.langfuse.com/#tag/ScoreConfigs/POST/api/public/score-configs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `categories` | body | `string` | no |
| `dataType` | body | `string` | no |
| `description` | body | `string` | no |
| `maxValue` | body | `string` | no |
| `minValue` | body | `string` | no |
| `name` | body | `string` | no |
