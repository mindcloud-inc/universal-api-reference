# Create Knowledge Base with Famulor AI - Voice Agent

Creates a new knowledge base in Famulor.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/knowledgebases`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Create Knowledge Base](https://docs.famulor.io/en/api-reference/knowledgebases/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Knowledge base description. |
| `name` | body | `string` | yes | Knowledge base name. |
