# Retrieve Related Object Counts with Rossum

Retrieves related object counts for a Rossum queue.

## Endpoint

- **Method:** `GET`
- **Path:** `/queues/:id/related_objects_counts`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Related Object Counts](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Queue ID whose related object counts should be retrieved. |
