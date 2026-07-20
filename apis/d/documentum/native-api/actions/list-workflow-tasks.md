# List Workflow Tasks with Documentum

## Endpoint

- **Method:** `GET`
- **Path:** `/repositories/{repositoryName}/tasklist`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [List Workflow Tasks](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `inline` | query | `boolean` | no | When true, include elaborated task details in the response. |
