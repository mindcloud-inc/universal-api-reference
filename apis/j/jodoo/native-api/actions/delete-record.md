# Delete Record with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/delete`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Delete Record](https://help.jodoo.com/en/articles/10335116-single-record-deletion-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID that owns the record. |
| `data_id` | body | `string` | yes | Jodoo record ID to delete. |
