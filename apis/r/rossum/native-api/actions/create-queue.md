# Create Queue with Rossum

Creates a new queue in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/queues`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Queue](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the queue to create. |
| `workspace` | body | `string` | yes | Workspace URL where the queue should be created. |
| `schema` | body | `string` | yes | Schema URL applied to annotations in the queue. |
