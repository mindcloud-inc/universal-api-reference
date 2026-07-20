# Run Query Form Search with Documentum

## Endpoint

- **Method:** `POST`
- **Path:** `/repositories/{repositoryName}/d2-saved-searches/queryforms/{queryFormId}/results`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Run Query Form Search](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `queryFormId` | path | `string` | yes | D2 saved search query form ID. |
| `queryRequest` | body | `object` | yes | Query form search request JSON payload. |
