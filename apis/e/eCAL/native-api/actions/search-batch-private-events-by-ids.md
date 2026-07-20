# Search Batch Private Events By IDs with ECAL

Finds batch private ECAL events by event IDs.

## Endpoint

- **Method:** `POST`
- **Path:** `/batch/events/search`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [Search Batch Private Events By IDs](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-list-of-events-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | JSON object matching ECAL's batch events search body, for example {"ids":["event-id"]}. |
