# Create Batch Private Events with ECAL

Creates batch private events in ECAL.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch/events`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Create Batch Private Events](https://docs.ecal.com/reference/private/batch.html#adding-private-batch-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's batch private event creation body, including an events array. |
