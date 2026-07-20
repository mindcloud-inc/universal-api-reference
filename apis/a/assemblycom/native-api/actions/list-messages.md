# List Messages with Assembly.com

Retrieves messages from an Assembly.com message channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Messages](https://docs.assembly.com/reference/list-messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | query | `string` | yes | The Message Channel to retrieve messages from. |
