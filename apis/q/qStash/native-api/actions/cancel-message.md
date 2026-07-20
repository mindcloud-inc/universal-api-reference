# Cancel Message with QStash

Cancels a queued or scheduled message in QStash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/messages/:messageId`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Cancel Message](https://upstash.com/docs/qstash/api-refence/messages/cancel-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Identifier of the message to cancel. |
