# List Gallery Assets with National Park Service

Retrieves gallery assets from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/multimedia/galleries/assets`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Gallery Assets](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `galleryId` | query | `string` | no | NPS gallery identifier. |
| `id` | query | `string` | no | NPS gallery asset identifier. |
