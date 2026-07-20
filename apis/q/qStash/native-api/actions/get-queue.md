# Get Queue with QStash

Retrieves a queue from QStash by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/queues/:queueName`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Get Queue](https://upstash.com/docs/qstash/api-refence/queues/get-a-queue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueName` | path | `string` | yes | Name of the queue to retrieve. |
