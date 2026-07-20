# List Categories By Location with InflatableOffice

Retrieves categories for a location from InflatableOffice.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories_list`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [List Categories By Location](https://rental.software/support/knowledge-base/article/api-categories-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | query | `number` | yes | Location ID to filter categories for a specific location. |
