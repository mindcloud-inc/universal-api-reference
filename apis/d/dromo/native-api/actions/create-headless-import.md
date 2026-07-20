# Create Headless Import with Dromo

Creates a new headless import in Dromo.

## Endpoint

- **Method:** `POST`
- **Path:** `/headless/imports/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Create Headless Import](https://developer.dromo.io/api-reference/headless/create-a-new-headless-import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | no | Request body field schema_id. |
| `original_filename` | body | `string` | no | Request body field original_filename. |
| `initial_data[]` | body | `array<string>` | no | Request body field initial_data. |
| `import_metadata` | body | `object` | no | Request body field import_metadata. |
