# Get All Resource Categories with Mews

Retrieves resource categories from Mews.

## Endpoint

- **Method:** `POST`
- **Path:** `/resourceCategories/getAll`
- **Base URL:** `{platformAddress}/api/connector/v1`
- **Official documentation:** [Get All Resource Categories](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/resourcecategories.md#get-all-resource-categories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ServiceIds[]` | body | `array<string>` | yes | Service identifiers whose resource categories should be returned. |
