# Get Call Queue with RingCentral

Retrieves a call queue from a RingCentral account.

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/call-queues/:groupId`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [Get Call Queue](https://developers.ringcentral.com/api-reference/Call-Queues/readCallQueueInfo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `groupId` | path | `string` | yes |
