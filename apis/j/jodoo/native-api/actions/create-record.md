# Create Record with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/create`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Create Record](https://help.jodoo.com/en/articles/9992387-single-record-creation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID to create a record in. |
| `data` | body | `object` | yes | Record field payload keyed by Jodoo widget IDs. Each widget must be an object with a value property, for example {"_widget_x":{"value":"Notebook"}}. |
