# Get DLQ Message with QStash

Retrieves a dead-letter queue message from QStash.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/dlq/:dlqId`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Get DLQ Message](https://upstash.com/docs/qstash/api-refence/dlq/get-a-dlq-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dlqId` | path | `string` | yes | DLQ ID of the message to retrieve. |
