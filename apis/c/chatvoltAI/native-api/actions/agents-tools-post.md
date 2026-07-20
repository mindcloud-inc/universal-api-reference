# Create Tool with Chatvolt AI

Creates a tool in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/agents/{agentId}/tools`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Create Tool](https://docs.chatvolt.ai/api-reference/endpoint/agents/tools/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | — |
| `type` | body | `string` | yes | Type for application/json requests. |
| `datastoreId` | body | `string` | no | Required when type is 'datastore'. |
| `formId` | body | `string` | no | Required when type is 'form'. |
| `isRaw` | body | `boolean` | no | Only applicable when type is 'http'. If true, the tool is configured with a raw cURL command. |
| `config` | body | `object` | no | Config for application/json requests. |
