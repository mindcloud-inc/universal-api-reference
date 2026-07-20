# List Forms with Jodoo

## Endpoint

- **Method:** `POST`
- **Path:** `/app/entry/list`
- **Base URL:** `https://api.jodoo.com/api/v5`
- **Official documentation:** [List Forms](https://help.jodoo.com/en/articles/9992378-user-form-query-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | body | `string` | yes | Jodoo app ID to list forms from. |
| `limit` | body | `number` | no | Maximum number of forms to return. |
| `skip` | body | `number` | no | Number of forms to skip before returning results. |
