# Update Score Config with Langfuse

Updates an existing score config in Langfuse.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/score-configs/:configId`
- **Base URL:** `https://cloud.langfuse.com/api/public`
- **Official documentation:** [Update Score Config](https://api.reference.langfuse.com/#tag/ScoreConfigs/PATCH/api/public/score-configs/{configId})

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `categories` | body | `string` | no |
| `configId` | path | `string` | no |
| `description` | body | `string` | no |
| `isArchived` | body | `string` | no |
| `maxValue` | body | `string` | no |
| `minValue` | body | `string` | no |
| `name` | body | `string` | no |
