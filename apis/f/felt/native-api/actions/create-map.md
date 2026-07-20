# Create Map with Felt

Creates a new map in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Map](https://developers.felt.com/rest-api/api-reference/maps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Map title. |
| `description` | body | `string` | no | Map description shown in the legend. |
| `public_access` | body | `string` | no | Map sharing level. |
| `basemap` | body | `string` | no | Basemap name or tile URL. |
| `lat` | body | `number` | no | Initial map latitude. |
| `lon` | body | `number` | no | Initial map longitude. |
| `zoom` | body | `number` | no | Initial map zoom level. |
