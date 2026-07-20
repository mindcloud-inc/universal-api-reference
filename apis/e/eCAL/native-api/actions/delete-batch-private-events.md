# Delete Batch Private Events with ECAL

Deletes batch private events from ECAL.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/batch/events`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Delete Batch Private Events](https://docs.ecal.com/reference/private/batch.html#deleting-private-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's batch private event deletion body, for example {"ids":["event-id"]}. |
