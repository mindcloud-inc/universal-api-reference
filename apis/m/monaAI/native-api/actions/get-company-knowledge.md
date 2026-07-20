# Get Company Knowledge with Mona AI

Retrieves company knowledge from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/companyKnowledge/getKnowledge`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Company Knowledge](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Knowledge category to retrieve. |
| `limit` | body | `number` | no | Maximum knowledge records to return. |
| `offset` | body | `number` | no | Offset for knowledge records. |
| `permission` | body | `string` | yes | Mona permission string required by the knowledge endpoint. |
