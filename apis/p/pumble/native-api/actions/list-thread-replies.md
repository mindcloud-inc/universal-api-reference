# List Thread Replies with Pumble

Retrieves replies for a Pumble thread message.

## Endpoint

- **Method:** `GET`
- **Path:** `/fetchThreadReplies`
- **Base URL:** `https://pumble-api-keys.addons.marketplace.cake.com`
- **Official documentation:** [List Thread Replies](https://pumble-api-keys.addons.marketplace.cake.com/api-docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `channel` | query | `string` | no |
| `channelId` | query | `string` | no |
| `cursor` | query | `string` | no |
| `limit` | query | `number` | no |
| `rootMessageId` | query | `string` | yes |
| `strategy` | query | `string` | no |
