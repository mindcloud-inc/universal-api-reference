# Publish Message with QStash

Publishes a message to a QStash destination.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/publish/:destination`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Publish Message](https://upstash.com/docs/qstash/api-refence/messages/publish-a-message)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | path | `string` | yes | Destination URL or URL Group name. |
| `body` | body | `string` | no | Raw request message to deliver. |
