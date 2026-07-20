# List Collections with Dynamic Mockups

Retrieves your collections from Dynamic Mockups.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/collections`
- **Base URL:** `https://app.dynamicmockups.com`
- **Official documentation:** [List Collections](https://docs.dynamicmockups.com/api-reference/get-collections-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_all_catalogs` | query | `boolean` | no | Set true to include collections across all catalogs. |
| `catalog_uuid` | query | `string` | no | Optional catalog UUID filter. |
