# Get Table Field with Caspio

Retrieves a table field from Caspio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/tables/{tableName}/fields/{fieldName}`
- **Base URL:** `https://d2hbw900.caspio.com/integrations/rest`
- **Official documentation:** [Get Table Field](https://d2hbw900.caspio.com/integrations/rest/swagger/index.html#/Tables/GetTableField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableName` | path | `string` | yes | Target table name. |
| `fieldName` | path | `string` | yes | Target field name. |
