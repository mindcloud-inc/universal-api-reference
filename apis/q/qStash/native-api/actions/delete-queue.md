# Delete Queue with QStash

Deletes an existing queue from QStash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/queues/:queueName`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Delete Queue](https://upstash.com/docs/qstash/api-refence/queues/delete-a-queue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueName` | path | `string` | yes | Name of the queue to delete. |
