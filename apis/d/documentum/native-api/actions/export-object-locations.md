# Export Object Locations with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/locations-export`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Export Object Locations](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object ID whose locations should be exported. |
| `export_type` | query | `string` | no | Locations export file type. The documented value is XLSX. |
| `file_name` | query | `string` | no | Optional custom locations export file name. |
