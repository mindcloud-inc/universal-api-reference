# Get Category Group with Statistics Netherlands CBS

Retrieves a category group from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/CategoryGroups({{id}})`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Category Group](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric category group row ID. Required by the OData key path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
