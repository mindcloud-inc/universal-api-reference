# List Batch Private Events By Reference Type with ECAL

Retrieves batch private events by ECAL reference type.

## Endpoint

- **Method:** `GET`
- **Path:** `/batch/events`
- **Base URL:** `https://api.ecal.com/apiv2`
- **Official documentation:** [List Batch Private Events By Reference Type](https://docs.ecal.com/reference/private/batch.html#retrieving-events-by-reference-type)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceType` | query | `string` | yes | Reference type used to retrieve private batch events. |
