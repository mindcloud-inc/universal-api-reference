# Get Book Tables with Timetonic

Retrieves tables for a book from Timetonic.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://timetonic.com/live/api.php`
- **Official documentation:** [Get Book Tables](https://timetonic.com/live/api.php?doc=#getBookTables-doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `b_c` | body | `string` | yes | Book code to inspect. |
| `b_o` | body | `string` | yes | Book owner to inspect. |
| `format` | body | `string` | no | Optional response format. Use android to include detailed table metadata. |
| `includeFields` | body | `string` | no | Optional flag to include field metadata. |
| `includeEnums` | body | `string` | no | Optional flag to include field enum metadata. |
| `getRowIds` | body | `string` | no | Optional flag to include view-to-row associations when using android format with field metadata. |
| `externViews` | body | `string` | no | Optional flag to include external views. |
