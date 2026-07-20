# Delete Live Security Rules For A Column with Sisense

Deletes live security rules for a Sisense column.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/elasticubes/live/:title/datasecurity/:table/:column`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Delete Live Security Rules For A Column](https://developer.sisense.com/guides/restApi/data-security.html#endpoints-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `column` | path | `string` | no | The column name. |
| `table` | path | `string` | no | The table name. |
| `title` | path | `string` | no | The live Datamodel title. |
