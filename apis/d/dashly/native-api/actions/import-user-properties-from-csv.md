# Import User Properties from CSV with Dashly

Imports user properties into Dashly from CSV.

## Endpoint

- **Method:** `POST`
- **Path:** `users/import`
- **Base URL:** `https://api.dashly.app`
- **Official documentation:** [Import User Properties from CSV](https://developers.dashly.io/webapi/endpoints/users/import/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `csvContent` | body | `string` | yes | CSV file contents including the header row. |
| `filename` | body | `string` | no | — |
| `merge_field` | body | `string` | no | — |
| `delimiter` | body | `string` | no | — |
| `tags` | body | `string` | no | Dashly tags payload, for example "\"super_tag\",\"import_tag_2\"". |
