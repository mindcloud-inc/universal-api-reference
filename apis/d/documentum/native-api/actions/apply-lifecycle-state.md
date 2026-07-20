# Apply Lifecycle State with Documentum

## Endpoint

- **Method:** `PUT`
- **Path:** `/repositories/{repositoryName}/d2-objects-lifecycle-state`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Apply Lifecycle State](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `properties` | body | `object` | yes | Lifecycle transition JSON payload, including object IDs, target state, signoff inputs, and optional properties bag as needed. |
