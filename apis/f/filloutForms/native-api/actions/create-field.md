# Create Field with Fillout Forms

Creates a field in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/fields`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Field](https://www.fillout.com/help/database/create-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | The unique identifier of the database |
| `tableId` | path | `string` | yes | The unique identifier of the table. You can also use the table name instead of the ID. |
| `type` | body | `list` | yes | Field type Accepted values: `attachments`, `autonumber`, `checkbox`, `currency`, `date`, `datetime`, `duration`, `email`, `linked_record`, `long_text`, `lookup`, `multiple_select`, `number`, `percent`, `phone_number`, `rating`, `single_line_text`, `single_select`, `source`, `url`. |
| `name` | body | `string` | yes | Field name |
| `template` | body | `object` | no | Field-specific configuration options. See the Fillout field types reference for the template shape for each field type. |
