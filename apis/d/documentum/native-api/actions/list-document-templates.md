# List Document Templates with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/document-templates`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [List Document Templates](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object ID. |
