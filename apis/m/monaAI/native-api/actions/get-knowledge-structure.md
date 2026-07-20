# Get Knowledge Structure with Mona AI

Retrieves the knowledge structure from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/companyKnowledge/getKnowledgeStructure`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Knowledge Structure](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeItemCounts` | body | `boolean` | no | Whether to include item counts in the knowledge structure. |
| `maxDepth` | body | `number` | no | Maximum folder depth to return. |
| `permission` | body | `string` | yes | Mona permission string required by the knowledge structure endpoint. |
