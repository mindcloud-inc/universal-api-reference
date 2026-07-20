# Run Quick Search with Documentum

## Endpoint

- **Method:** `POST`
- **Path:** `/repositories/{repositoryName}/quickSearch`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Run Quick Search](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `searchRequest` | body | `object` | yes | Quick search request JSON payload. |
