# Apply Template To Object with Documentum

## Endpoint

- **Method:** `POST`
- **Path:** `/repositories/{repositoryName}/objects-d2/{objectId}`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Apply Template To Object](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `objectId` | path | `string` | yes | Documentum object ID to update with a template. |
| `properties` | body | `object` | yes | JSON properties payload, for example template_name and folder_id. |
