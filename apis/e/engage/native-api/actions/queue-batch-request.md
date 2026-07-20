# Queue Batch Request with Engage

Queues batched user creates, updates, and events in Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Queue Batch Request](https://docs.engage.so/en-us/a/634d516c3713733fec88a7d4-batch-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of batch request items to queue. |
