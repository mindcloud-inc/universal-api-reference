# Delete File with Moorcheh

Deletes files from a Moorcheh namespace in storage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/namespaces/:namespace_name/delete-file`
- **Base URL:** `https://api.moorcheh.ai/v1`
- **Official documentation:** [Delete File](https://docs.moorcheh.ai/api-reference/data/delete-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespace_name` | path | `string` | yes | Namespace that contains the file or files. |
| `file_name` | body | `string` | yes | Single file to permanently delete, such as document.pdf. |
| `file_names[]` | body | `array<string>` | no | Multiple file names to permanently delete in one request. |
