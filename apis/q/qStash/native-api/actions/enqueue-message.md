# Enqueue Message with QStash

Enqueues a message in a QStash queue.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/enqueue/:queueName/:destination`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Enqueue Message](https://upstash.com/docs/qstash/api-refence/messages/enqueue-a-message)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queueName` | path | `string` | yes | Queue name to enqueue the message to. |
| `destination` | path | `string` | yes | Destination URL or URL Group name. |
| `body` | body | `string` | no | Raw request message to deliver. |
