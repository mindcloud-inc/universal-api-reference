# List Locations with RO App

## Endpoint

- **Method:** `GET`
- **Path:** `/company/locations`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [List Locations](https://roapp.readme.io/reference/get-company-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_archived` | query | `boolean` | no | Filters locations by archived status |
| `legal_entity_id` | query | `number` | no | Legal entity ID |
| `sort` | query | `string` | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |
