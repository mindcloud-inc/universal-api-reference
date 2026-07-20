# Create D2 Object with Documentum

## Endpoint

- **Method:** `POST`
- **Path:** `/repositories/{repositoryName}/object-creation`
- **Base URL:** `{documentumRestBaseUrl}`
- **Official documentation:** [Create D2 Object](https://opentext.github.io/d2sv-sdk/24.4.0/bundle/pdf/OpenText%20Documentum%20D2FS%20REST%20Services%20Development%20Guide.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `repositoryName` | path | `string` | yes | Documentum repository name. |
| `properties` | body | `object` | yes | JSON object properties for creation, including r_object_type, object_name, and D2 configuration values as needed. |
