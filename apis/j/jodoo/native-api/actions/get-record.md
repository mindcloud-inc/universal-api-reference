# Get Record with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/data/get`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [Get Record](https://help.jodoo.com/en/articles/9992384-single-record-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID that owns the form. |
| `entry_id` | body | `string` | yes | Jodoo form ID. |
| `data_id` | body | `string` | yes | Jodoo record ID to fetch. |
