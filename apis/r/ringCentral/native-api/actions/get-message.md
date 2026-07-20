# Get Message with RingCentral

Retrieves a message from a RingCentral extension.

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/extension/:extensionId/message-store/:messageId`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [Get Message](https://developers.ringcentral.com/api-reference/Message-Store/readMessage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `extensionId` | path | `string` | yes |
| `messageId` | path | `string` | yes |
