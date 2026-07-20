# Create Contact Custom Field with Aspire

Creates a new contact custom field in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `ContactCustomFields`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Contact Custom Field](https://guide.youraspire.com/apidocs/propertycustomfields-7)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ContactCustomFieldDefinitionID` | body | `number` | yes |
| `ContactID` | body | `number` | yes |
| `ColumnValue` | body | `string` | yes |
