# Update Records with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/batch_update`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Update Records](https://help.jodoo.com/en/articles/10335100-multiple-records-update-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID that owns the records. |
| `data_ids` | body | `object<string>` | yes | JSON array of record IDs for Jodoo `data_ids`. |
| `data` | body | `object` | yes | Field payload applied to every selected record. Each widget value must be wrapped in an object with a `value` property. |
