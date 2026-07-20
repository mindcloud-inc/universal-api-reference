# Delete BOM with MRPeasy

Deletes an existing BOM from MRPeasy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/boms/{{bomId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Delete BOM](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bom_id` | path | `number` | yes | MRPeasy BOM ID. |
