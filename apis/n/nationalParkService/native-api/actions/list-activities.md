# List Activities with National Park Service

Retrieves activities from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Activities](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Activity unique ID. |
| `q` | query | `string` | no | Search term. |
