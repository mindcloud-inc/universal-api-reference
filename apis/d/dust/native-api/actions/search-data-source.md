# Search Data Source with Dust

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspaceId/spaces/:spaceId/data_sources/:dataSourceId/search`
- **Base URL:** `https://dust.tt`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSourceId` | path | `string` | yes | Dust data source sId. |
| `query` | body | `string` | yes | Search query string. |
| `spaceId` | path | `string` | yes | Dust space sId. |
