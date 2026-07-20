# Get Search Configuration with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/search-configuration/{configId}`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Get Search Configuration](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `configId` | path | `string` | yes | Object ID of the D2 search configuration. |
