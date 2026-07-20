# Publish Message with Upstash Redis

Publishes a message to an Upstash Redis channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/publish/:channel/:message`
- **Base URL:** `https://choice-oriole-98954.upstash.io`
- **Official documentation:** [Publish Message](https://upstash.com/docs/redis/features/restapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | path | `string` | yes | Channel name to publish to. |
| `message` | path | `string` | yes | Message payload to publish. |
