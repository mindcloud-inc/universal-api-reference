# Link Contact to Dispatch with Chatvolt AI

Links a contact to a dispatch in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/dispatches/contacts/link`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Link Contact to Dispatch](https://docs.chatvolt.ai/api-reference/endpoint/dispatches/contacts/link/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dispatchId` | body | `string` | no | DispatchId for application/json requests. |
| `contactListId` | body | `string` | no | ContactListId for application/json requests. |
| `isExcluded` | body | `boolean` | no | Set to true to exclude this list from the dispatch. |
