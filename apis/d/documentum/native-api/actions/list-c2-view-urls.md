# List C2 View URLs with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/views/c2-view`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [List C2 View URLs](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object ID with a PDF source or rendition. |
