# List Files with Anthropic

Retrieves uploaded files from the Anthropic account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Files](https://platform.claude.com/docs/en/api/beta/files/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of files to return. |
| `after_id` | query | `string` | no | Return items after this file ID for forward pagination. |
| `before_id` | query | `string` | no | Return items before this file ID for reverse pagination. |
