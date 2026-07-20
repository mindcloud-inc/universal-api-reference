# Pause Queue with QStash

Pauses an existing queue in QStash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/queues/:queueName/pause`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Pause Queue](https://upstash.com/docs/qstash/api-refence/queues/pause-queue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueName` | path | `string` | yes | Name of the queue to pause. |
