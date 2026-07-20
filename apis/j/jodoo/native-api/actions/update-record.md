# Update Record with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/update`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Update Record](https://help.jodoo.com/en/articles/9992411-single-record-update-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID that owns the record. |
| `data_id` | body | `string` | yes | Jodoo record ID to update. |
| `data` | body | `object` | yes | Updated field payload keyed by Jodoo widget IDs. Each widget must be an object with a value property, for example {"_widget_x":{"value":"Updated Item"}}. |
