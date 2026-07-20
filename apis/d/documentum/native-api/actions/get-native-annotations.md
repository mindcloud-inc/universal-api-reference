# Get Native Annotations with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/objects/{objectId}/native-annotations-for-collaboration-edit`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Native Annotations](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum document or task object ID. |
| `inline` | query | `boolean` | no | When true, return annotation details inline. |
