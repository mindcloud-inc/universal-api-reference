# Get Audit Trail Event Source Facets with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/audit-trail-facets-by-event-source`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Audit Trail Event Source Facets](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object ID whose audit facets should be returned. |
| `all_versions` | query | `boolean` | no | When true, include all versions when grouping audit facets. |
| `filter` | query | `string` | no | Optional audit filter expression. |
