# Get Conversation Parts with Dashly

Retrieves parts from a Dashly conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `conversations/:id/parts`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Get Conversation Parts](https://developers.dashly.io/webapi/endpoints/conversations/parts/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `id_as_string` | query | `boolean` | no |
