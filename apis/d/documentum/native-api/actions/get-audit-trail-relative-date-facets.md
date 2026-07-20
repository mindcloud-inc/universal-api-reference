# Get Audit Trail Relative Date Facets with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/audit-trail-facets-by-relative-date`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Audit Trail Relative Date Facets](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object ID whose audit facets should be returned. |
| `event_source` | query | `string` | no | Audit event source: Automatic, Manual, or All. Defaults to All. |
