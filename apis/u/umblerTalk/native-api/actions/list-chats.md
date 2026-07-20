# List Chats with Umbler Talk

Retrieves chats from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Chats](https://app-utalk.umbler.com/api/docs/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | query | `string` | yes | The organization ID. |
