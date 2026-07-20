# Update Queue with Rossum

Updates a queue in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/queues/:id`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Queue](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Rossum queue ID. |
| `name` | body | `string` | no | Updated queue name. |
