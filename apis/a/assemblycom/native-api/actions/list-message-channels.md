# List Message Channels with Assembly.com

Retrieves message channels from Assembly.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/message-channels`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Message Channels](https://docs.assembly.com/reference/list-message-channels)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `membershipType` | query | `string` | no | — |
| `clientId` | query | `string` | no | Only return individual channels for this client. |
| `memberId` | query | `string` | no | Only return channels that contain the member matching this ID. |
| `membershipEntityId` | query | `string` | no | Deprecated. Use clientId instead. |
