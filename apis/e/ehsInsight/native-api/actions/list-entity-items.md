# List Entity Items with EHS Insight

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/entity/:entityName/list`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [List Entity Items](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityName` | path | `string` | yes | — |
| `queryParameters[]` | query | `array<object>` | no | Optional query parameters. Add one Field/Value row per query parameter. The Field dropdown suggests documented names; custom field names are also accepted. |
| `queryParameters[].field` | query | `list<string>` | no | Select a documented query parameter or supply a custom field name. Accepted values: `ChangeTokenAfter`, `ChangeTokenBefore`, `CreatedAfter`, `CreatedBefore`, `Fields`, `UpdatedAfter`, `UpdatedBefore`. |
| `queryParameters[].value` | query | `string` | no | Value for the selected query parameter. Use UTC date/time text for date parameters and comma-separated names for Fields. |
