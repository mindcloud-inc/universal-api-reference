# Assign to User with Chatvolt AI

Assigns a conversation to a user in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{conversationId}/assign`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Assign to User](https://docs.chatvolt.ai/api-reference/endpoint/conversation/assign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation to be assigned. |
| `email` | body | `string` | yes | Email of the user to whom the conversation will be assigned. |
| `id` | body | `string` | no | ID of the user to whom the conversation will be assigned. |
| `membershipId` | body | `string` | no | ID of the membership to whom the conversation will be assigned. |
