# Delete Records with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/batch_delete`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Delete Records](https://help.jodoo.com/en/articles/9992415-multiple-records-deletion-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID that owns the records. |
| `data_ids` | body | `object<string>` | yes | JSON array of record IDs for Jodoo `data_ids`. |
