# Check Key Exists with Upstash Redis

Checks whether a key exists in Upstash Redis.

## Endpoint

- **Method:** `GET`
- **Path:** `/exists/:key`
- **Base URL:** `https://choice-oriole-98954.upstash.io`
- **Official documentation:** [Check Key Exists](https://upstash.com/docs/redis/features/restapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Redis key to check. |
