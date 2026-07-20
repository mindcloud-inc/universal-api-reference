# Get Key TTL with Upstash Redis

Retrieves a key TTL from Upstash Redis.

## Endpoint

- **Method:** `GET`
- **Path:** `/ttl/:key`
- **Base URL:** `https://choice-oriole-98954.upstash.io`
- **Official documentation:** [Get Key TTL](https://upstash.com/docs/redis/features/restapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Redis key whose TTL to inspect. |
