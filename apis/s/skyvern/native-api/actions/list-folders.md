# List Folders with Skyvern

Retrieves workflow folders for your organization from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/folders`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [List Folders](https://www.skyvern.com/docs/api-reference/workflows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search folders by title or description |
