# Create Collection with Dynamic Mockups

Creates a new collection in Dynamic Mockups.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/collections`
- **Base URL:** `https://app.dynamicmockups.com`
- **Official documentation:** [Create Collection](https://docs.dynamicmockups.com/api-reference/get-collections-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the collection to create. |
| `catalog_uuid` | body | `string` | no | Optional catalog UUID to place this collection in. |
