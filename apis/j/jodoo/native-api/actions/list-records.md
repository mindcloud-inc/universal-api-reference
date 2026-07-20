# List Records with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/list`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [List Records](https://help.jodoo.com/en/articles/9992385-multiple-records-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID to query. |
| `limit` | body | `number` | no | Maximum number of records to return. |
| `data_id` | body | `string` | no | Optional cursor record ID used to continue pagination. |
