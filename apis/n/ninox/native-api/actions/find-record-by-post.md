# Find Record By POST with Ninox

Finds a record in Ninox by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:teamid/databases/:dbid/tables/:tableid/record`
- **Base URL:** `https://api.ninox.com/v1`
- **Official documentation:** [Find Record By POST](https://forum.ninox.com/t/35yzp89/api-endpoints-for-public-cloud)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamid` | path | `string` | yes | Workspace ID that owns the database. |
| `dbid` | path | `string` | yes | Database ID that owns the table. |
| `tableid` | path | `string` | yes | Table ID to search. |
| `style` | query | `string` | no | Optional response style. |
| `dateStyle` | query | `string` | no | Optional date formatting style. |
| `choiceStyle` | query | `string` | no | Optional choice formatting style. |
| `filters` | body | `object` | yes | Filter object used to find one record. |
