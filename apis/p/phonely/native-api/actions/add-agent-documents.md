# Add Agent Documents with Phonely

Adds documents to a Phonely agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/agent-documents`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Add Agent Documents](https://docs.phonely.ai/api-reference/endpoint/post-agent-documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | Your Phonely user ID. |
| `agentId` | body | `string` | yes | The ID of the agent whose knowledge base will receive the upload. |
| `files` | body | `file` | yes | Document file to upload. Phonely supports PDF, DOCX, and TXT files up to 10 MB each. |
