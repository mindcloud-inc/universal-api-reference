# List Workers with InflatableOffice

Retrieves workers from InflatableOffice.

## Endpoint

- **Method:** `GET`
- **Path:** `/workers`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [List Workers](https://rental.software/support/knowledge-base/article/api-workers-retrieve-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_body` | query | `boolean` | no | When true, returns more worker details. |
| `approved` | query | `boolean` | no | When true, returns only approved workers. |
| `vehicle` | query | `boolean` | no | When true, returns vehicles instead of workers. |
