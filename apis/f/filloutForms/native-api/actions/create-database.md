# Create Database with Fillout Forms

Creates a database in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Database](https://www.fillout.com/help/database/create-database)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Database name |
| `tables[]` | body | `array<object>` | yes | Array of table definitions to create with the database |
| `tables[].name` | body | `string` | yes | Table name |
| `tables[].fields[]` | body | `array<object>` | yes | Array of field definitions to create with the table |
| `tables[].fields[].type` | body | `list` | yes | Field type Accepted values: `attachments`, `autonumber`, `checkbox`, `currency`, `date`, `datetime`, `duration`, `email`, `linked_record`, `long_text`, `lookup`, `multiple_select`, `number`, `percent`, `phone_number`, `rating`, `single_line_text`, `single_select`, `source`, `url`. |
| `tables[].fields[].name` | body | `string` | yes | Field name |
| `tables[].fields[].template` | body | `object` | yes | Field-specific configuration options. See the Fillout field types reference for the template shape for each field type. |
