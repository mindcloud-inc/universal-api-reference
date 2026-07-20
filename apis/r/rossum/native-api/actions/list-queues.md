# List Queues with Rossum

Retrieves queues from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/queues`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Queues](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ordering` | query | `string` | no | Ordering expression, for example name or -name. |
| `workspace` | query | `number` | no | Filter queues by Rossum workspace ID. |
