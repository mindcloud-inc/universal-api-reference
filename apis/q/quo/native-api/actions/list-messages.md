# List Messages with Quo

Retrieves all messages from Quo.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.openphone.com/v1`
- **Official documentation:** [List Messages](https://www.quo.com/docs/mdx/api-reference/messages/list-messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdAfter` | query | `date` | no |
| `createdBefore` | query | `date` | no |
| `participants[]` | query | `array<string>` | yes |
| `phoneNumberId` | query | `string` | yes |
| `userId` | query | `string` | no |
