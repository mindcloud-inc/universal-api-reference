# List Properties with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `properties`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [List Properties](https://api-portal.centerpointconnect.io/portal/catalogue-products/centerpoint-api-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/propertiesGET)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | An special argument to sort by selected attribute, use no opperators for ascending order and a minus operator for descending order and input the attribute next to it. e.g. "-createdAt" |
| `filter[updated_at][gt]` | query | `string` | no | — |
| `include` | query | `string` | no | e.g. = manager,company,primaryContractor,location,integrationRelations |
| `fields[properties]` | query | `string` | no | Optional fields properties query parameter. |
| `fields[profiles]` | query | `string` | no | Optional fields profiles query parameter. |
| `fields[companies]` | query | `string` | no | Optional fields companies query parameter. |
| `fields[locations]` | query | `string` | no | Optional fields locations query parameter. |
