# Export Object Audit with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/audit-export`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Export Object Audit](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object or workflow ID whose audit should be exported. |
| `all_versions` | query | `boolean` | no | When true, export audit data for all versions. Defaults to true. |
| `export_type` | query | `string` | no | Audit export file type. The documented value is XLSX. |
| `filter` | query | `string` | no | Optional audit filter expression. |
| `file_name` | query | `string` | no | Optional custom audit export file name. |
