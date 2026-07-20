# Delete Agent Documents with Phonely

Deletes agent documents from Phonely.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/agent-documents`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Delete Agent Documents](https://docs.phonely.ai/api-reference/endpoint/delete-agent-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | query | `string` | yes | Your Phonely user ID. |
| `agentId` | query | `string` | yes | The ID of the agent that owns the document. |
| `documentId` | query | `string` | yes | The ID of the knowledge-base document to delete. |
