# List Batch Private Events By Subscriber with ECAL

Retrieves batch private events for one ECAL subscriber.

## Endpoint

- **Method:** `GET`
- **Path:** `/batch/events`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [List Batch Private Events By Subscriber](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-subscriber-id)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecal_id` | query | `string` | yes | Subscriber ecal_id value for batch private event retrieval. |
