# Resume Queue with QStash

Resumes a paused queue in QStash.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/queues/:queueName/resume`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Resume Queue](https://upstash.com/docs/qstash/api-refence/queues/resume-queue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueName` | path | `string` | yes | Name of the queue to resume. |
