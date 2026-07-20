# List Conversations with Quo

Retrieves all existing conversations from Quo.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [List Conversations](https://www.quo.com/docs/mdx/api-reference/conversations/list-conversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdAfter` | query | `date` | no |
| `createdBefore` | query | `date` | no |
| `excludeInactive` | query | `boolean` | no |
| `phoneNumbers[]` | query | `array<string>` | no |
| `updatedAfter` | query | `date` | no |
| `updatedBefore` | query | `date` | no |
| `userId` | query | `string` | no |
