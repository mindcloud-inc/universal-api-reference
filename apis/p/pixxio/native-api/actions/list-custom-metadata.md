# List Custom Metadata with pixx.io

Retrieves custom metadata fields from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/metadata/custom`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [List Custom Metadata](https://api.pixxio.com/docs/openapi)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `responseFields` | query | `string` | no | Custom metadata fields to include in the response. Send multiple values as a array. |
