# List Categories By WordPress Sync with InflatableOffice

Retrieves categories for a WordPress sync from InflatableOffice.

## Endpoint

- **Method:** `GET`
- **Path:** `/categories_list`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [List Categories By WordPress Sync](https://rental.software/support/knowledge-base/article/api-categories-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wpid` | query | `number` | yes | WordPress sync entry ID to filter categories for a specific WordPress sync. |
