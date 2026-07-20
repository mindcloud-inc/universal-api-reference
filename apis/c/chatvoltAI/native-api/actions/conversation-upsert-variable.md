# Create/Update Custom Variable with Chatvolt AI

Creates a custom variable in Chatvolt AI, or updates an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/variables`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create/Update Custom Variable](https://docs.chatvolt.ai/api-reference/endpoint/conversation/upsert-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | body | `string` | yes | ID of the conversation to which the variable belongs. |
| `varName` | body | `string` | yes | Variable name (key). |
| `varValue` | body | `string` | yes | Variable value. |
