# Create Message Channel with Assembly.com

Creates a message channel in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/message-channels`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Create Message Channel](https://docs.assembly.com/reference/create-message-channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `membershipType` | body | `string` | yes | The type of membership this channel is associated with. |
| `clientId` | body | `string` | no | The id of the client this channel is for. |
| `companyId` | body | `string` | no | The id of the company this channel belongs to. |
| `memberIds[]` | body | `array<string>` | no | The client IDs to add to a group channel. |
| `membershipEntityId` | body | `string` | no | Deprecated. Use clientId and companyId instead. |
