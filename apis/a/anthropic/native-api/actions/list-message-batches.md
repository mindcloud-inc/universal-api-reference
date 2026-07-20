# List Message Batches with Anthropic

Retrieves message batches from the Anthropic account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/messages/batches`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [List Message Batches](https://platform.claude.com/docs/en/api/messages/batches/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_id` | query | `string` | no | Return results before this message batch ID. |
| `after_id` | query | `string` | no | Return results after this message batch ID. |
| `limit` | query | `number` | no | Number of items to return per page. |
