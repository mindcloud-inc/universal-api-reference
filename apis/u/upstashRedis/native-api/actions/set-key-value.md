# Set Key Value with Upstash Redis

Sets a key value in Upstash Redis.

## Endpoint

- **Method:** `GET`
- **Path:** `/set/:key/:value`
- **Base URL:** `https://choice-oriole-98954.upstash.io`
- **Official documentation:** [Set Key Value](https://upstash.com/docs/redis/features/restapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Redis key to create or overwrite. |
| `value` | path | `string` | yes | String value to store. |
