# List Messages with RingCentral

Retrieves messages from a RingCentral extension.

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/extension/:extensionId/message-store`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [List Messages](https://developers.ringcentral.com/api-reference/Message-Store/listMessages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `extensionId` | path | `string` | yes |
| `messageType` | query | `string` | no |
| `dateTo` | query | `string` | no |
