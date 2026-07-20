# List categorypages with Wisewand

Retrieves category pages from your Wisewand workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/categorypages/`
- **Base URL:** `https://api.wisewand.ai`
- **Official documentation:** [List categorypages](https://api.wisewand.ai/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Wisewand query parameter `search`. |
| `maker` | query | `string` | no | Wisewand query parameter `maker`. |
| `status` | query | `string` | no | Wisewand query parameter `status`. |
| `projectId` | query | `string` | no | Wisewand query parameter `projectId`. |
| `persona` | query | `string` | no | Wisewand query parameter `persona`. |
| `author` | query | `string` | no | Wisewand query parameter `author`. |
| `category` | query | `string` | no | Wisewand query parameter `category`. |
| `published` | query | `string` | no | Wisewand query parameter `published`. |
