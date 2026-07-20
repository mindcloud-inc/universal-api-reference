# List Locations with Storerocket

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/locations`
- **Base URL:** `https://storerocket.io/api/v2`
- **Official documentation:** [List Locations](https://storerocket.io/api/v2/projects/:projectId/locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The StoreRocket project ID that owns the locations. |
| `page` | query | `number` | no | Page number for the paginated locations list. |
| `limit` | query | `number` | no | Maximum number of locations returned per page. Verified live against the StoreRocket API. |
