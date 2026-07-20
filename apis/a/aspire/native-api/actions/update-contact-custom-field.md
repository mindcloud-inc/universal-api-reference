# Update Contact Custom Field with Aspire

Updates an existing contact custom field in your Aspire account.

## Endpoint

- **Method:** `PUT`
- **Path:** `ContactCustomFields`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Contact Custom Field](https://guide.youraspire.com/apidocs/propertycustomfields-7)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ContactCustomFieldValueID` | body | `number` | yes |
| `ColumnValue` | body | `string` | yes |
