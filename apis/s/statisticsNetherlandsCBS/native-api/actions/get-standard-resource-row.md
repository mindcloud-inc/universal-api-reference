# Get Standard Resource Row with Statistics Netherlands CBS

Retrieves a standard resource row from a Statistics Netherlands CBS table.

## Endpoint

- **Method:** `GET`
- **Path:** `/ODataApi/odata/{{tableIdentifier}}/{{resourceName}}('{{key}}')`
- **Base URL:** `https://opendata.cbs.nl`
- **Official documentation:** [Get Standard Resource Row](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | The string Key value for the row in the named table-specific resource. |
| `resourceName` | path | `string` | yes | Named entity set in the table service, such as a dimension resource. Required by the service path. |
| `tableIdentifier` | path | `string` | yes | CBS StatLine table identifier, for example 83765NED. Required by the service path. |
