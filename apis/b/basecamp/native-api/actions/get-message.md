# Get Message with Basecamp

Retrieves a message from Basecamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/:accountId/messages/:messageId.json`
- **Base URL:** `https://3.basecampapi.com`
- **Official documentation:** [Get Message](https://github.com/basecamp/bc3-api/blob/master/sections/messages.md#get-a-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `messageId` | path | `number` | yes |
