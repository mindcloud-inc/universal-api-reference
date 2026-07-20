# List Topics with National Park Service

Retrieves topics from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/topics`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Topics](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Topic unique ID. |
| `q` | query | `string` | no | Search term. |
