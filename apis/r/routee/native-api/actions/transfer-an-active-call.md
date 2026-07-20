# Transfer an active call with Routee

Transfers an active call in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/conversation/:messageId/transfer`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Transfer an active call](https://docs.routee.net/reference/transfer-an-active-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The id of the voice call to be transfered. |
| `from` | body | `string` | yes | The sender Id for this call |
| `to` | body | `object` | yes | The recipient of the call |
| `hangupDelay` | body | `number` | no | The time to wait for the call to be answered. |
| `maxDuration` | body | `number` | no | Defines the maximum duration. |
| `callback` | body | `object` | no | Defines the notification callback information for the progress of the Voice call. |
