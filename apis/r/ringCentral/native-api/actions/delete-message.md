# Delete Message with RingCentral

Deletes a message from a RingCentral extension.

## Endpoint

- **Method:** `DELETE`
- **Path:** `restapi/v1.0/account/:accountId/extension/:extensionId/message-store/:messageId`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [Delete Message](https://developers.ringcentral.com/api-reference/Message-Store/deleteMessage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `extensionId` | path | `string` | yes |
| `messageId` | path | `string` | yes |
