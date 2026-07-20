# Create Table with Fillout Forms

Creates a table in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Table](https://www.fillout.com/help/database/create-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database |
| `name` | body | `string` | yes | Table name |
| `fields[]` | body | `array<object>` | yes | Array of field definitions to create with the table |
| `fields[].type` | body | `list` | yes | Field type Accepted values: `attachments`, `autonumber`, `checkbox`, `currency`, `date`, `datetime`, `duration`, `email`, `linked_record`, `long_text`, `lookup`, `multiple_select`, `number`, `percent`, `phone_number`, `rating`, `single_line_text`, `single_select`, `source`, `url`. |
| `fields[].name` | body | `string` | yes | Field name |
| `fields[].template` | body | `object` | yes | Field-specific configuration options. See the Fillout field types reference for the template shape for each field type. |
