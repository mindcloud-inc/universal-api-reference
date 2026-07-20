# List Batch Private Events By Subscriber And Reference Type with ECAL

Retrieves batch private events by subscriber and reference type.

## Endpoint

- **Method:** `GET`
- **Path:** `/batch/events`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [List Batch Private Events By Subscriber And Reference Type](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-subscriber-id-and-reference-type)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ecal_id` | query | `string` | yes | Subscriber ecal_id value for batch private event retrieval. |
| `referenceType` | query | `string` | yes | Reference type used with subscriber ecal_id for batch private event retrieval. |
