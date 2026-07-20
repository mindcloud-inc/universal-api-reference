# Update BOM with MRPeasy

Updates an existing BOM in MRPeasy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/boms/{{bomId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Update BOM](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bom_id` | path | `number` | yes | MRPeasy BOM ID. |
| `title` | body | `string` | no | Updated BOM title. |
| `components` | body | `array<object>` | no | Updated BOM components array. |
