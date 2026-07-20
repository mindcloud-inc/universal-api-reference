# Get Knowledge Base Document with Famulor AI - Voice Agent

Retrieves document details from a Famulor knowledge base.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/knowledgebases/:knowledgebaseId/documents/:id`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Get Knowledge Base Document](https://docs.famulor.io/en/api-reference/knowledgebases/get-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Knowledge base document ID. |
| `knowledgebaseId` | path | `number` | yes | Famulor knowledge base ID. |
