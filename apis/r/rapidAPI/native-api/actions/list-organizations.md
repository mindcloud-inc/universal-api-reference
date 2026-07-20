# List Organizations with RapidAPI

Retrieves organizations from RapidAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/organizations`
- **Base URL:** `{baseUrlRest}`
- **Official documentation:** [List Organizations](https://docs.rapidapi.com/docs/managing-collections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Organization status filter. |
| `limit` | query | `number` | no | Maximum number of organizations to return. |
