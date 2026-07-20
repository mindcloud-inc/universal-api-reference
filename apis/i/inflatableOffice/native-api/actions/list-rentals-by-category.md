# List Rentals By Category with InflatableOffice

Retrieves rentals by category from InflatableOffice.

## Endpoint

- **Method:** `GET`
- **Path:** `/rentals`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [List Rentals By Category](https://rental.software/support/knowledge-base/article/api-rentals-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryid` | query | `string` | yes | ID of the category whose rentals should be returned. |
