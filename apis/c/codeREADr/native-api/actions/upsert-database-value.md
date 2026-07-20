# Upsert Database Value with CodeREADr

Adds or updates a database value in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Upsert Database Value](https://secure.codereadr.com/apidocs/Databases.md#upsertvalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | body | `string` | yes | Database to update. |
| `value` | body | `string` | yes | Barcode value to insert or update. |
| `response` | body | `string` | no | Associated response text for the barcode. |
| `validity` | body | `string` | no | Set to 1 for valid or 0 for invalid. |
| `trim_value` | body | `string` | no | Trim surrounding whitespace before saving. |
