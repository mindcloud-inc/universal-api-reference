# Create Records with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/batch_create`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Create Records](https://help.jodoo.com/en/articles/9992388-multiple-records-creation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID to create records in. |
| `data_list` | body | `object<object>` | yes | JSON array of record payload objects for Jodoo `data_list`. Each record must be keyed by widget IDs, and every widget value must be wrapped in an object with a `value` property. |
