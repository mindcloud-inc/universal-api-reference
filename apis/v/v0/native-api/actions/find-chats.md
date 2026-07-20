# Find Chats with v0

Finds chats in the v0 workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Find Chats](https://v0.app/docs/api/platform/reference/chats/find)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
| `isFavorite` | query | `string` | no | Filter chats by whether they are marked as favorites. |
| `vercelProjectId` | query | `string` | no | — |
| `branch` | query | `string` | no | — |
