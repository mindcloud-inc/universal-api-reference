# Upsert Queue with QStash

Creates a QStash queue, or updates one if it exists.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/queues`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Upsert Queue](https://upstash.com/docs/qstash/api-refence/queues/upsert-a-queue)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueName` | body | `string` | yes | The name of the queue. |
| `parallelism` | body | `number` | yes | Number of parallel consumers consuming from the queue. |
