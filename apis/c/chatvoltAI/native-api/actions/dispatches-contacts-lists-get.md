# Get Contact Lists with Chatvolt AI

Retrieves contact lists from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/dispatches/contacts/lists`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get Contact Lists](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/lists/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `search` | query | `string` | no | Search term for contact list name. |
