# Get Message with QStash

Retrieves a message from QStash by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/messages/:messageId`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Get Message](https://upstash.com/docs/qstash/api-refence/messages/get-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Identifier of the message to retrieve. |
