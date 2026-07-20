# Bulk Upsert Database Values with CodeREADr

Adds or updates multiple database values in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Bulk Upsert Database Values](https://secure.codereadr.com/apidocs/Databases.md#upsertmultivalue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_id` | body | `number` | no | Optional global database ID applied to values that do not specify their own databaseId. |
| `trim_value` | body | `number` | no | Optional global trim flag applied to values that do not specify their own trimValue. |
| `values[]` | body | `array<object>` | yes | Array of up to 100 objects. Each item requires value and may include databaseId, trimValue, response, and validity. |
