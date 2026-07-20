# List Mockups with Dynamic Mockups

Retrieves your mockups from Dynamic Mockups.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/mockups`
- **Base URL:** `https://app.dynamicmockups.com`
- **Official documentation:** [List Mockups](https://docs.dynamicmockups.com/api-reference/get-mockups-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_all_catalogs` | query | `boolean` | no | Set true to include mockups across all catalogs. |
| `catalog_uuid` | query | `string` | no | Optional catalog UUID filter. |
| `collection_uuid` | query | `string` | no | Optional collection UUID filter. |
| `name` | query | `string` | no | Optional name filter. |
