# Delete Key with Upstash Redis

Deletes a key from Upstash Redis.

## Endpoint

- **Method:** `GET`
- **Path:** `/del/:key`
- **Base URL:** `https://choice-oriole-98954.upstash.io`
- **Official documentation:** [Delete Key](https://upstash.com/docs/redis/features/restapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | Redis key to delete. |
