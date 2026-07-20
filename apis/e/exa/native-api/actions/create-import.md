# Create Import with Exa

Creates a new import in Exa.

## Endpoint

- **Method:** `POST`
- **Path:** `/websets/v0/imports`
- **Base URL:** `https://api.exa.ai`
- **Official documentation:** [Create Import](https://exa.ai/docs/websets/api/imports/create-an-import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | yes | Number of records in the import. |
| `csv.identifier` | body | `number` | no | CSV column index or identifier column setting. |
| `entity.type` | body | `string` | yes | Entity type for imported records. |
| `format` | body | `string` | yes | Import format, such as csv. |
| `metadata` | body | `object` | no | Optional import metadata object. |
| `size` | body | `number` | yes | Size of the import file in bytes. |
| `title` | body | `string` | no | Optional import title. |
