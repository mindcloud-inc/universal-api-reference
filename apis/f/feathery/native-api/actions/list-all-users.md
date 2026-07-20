# List All Users with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/user/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List All Users](https://api-docs.feathery.io/#list-all-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `date` | no | Limit users to after this creation time. |
| `created_before` | query | `date` | no | Limit users to before this creation time. |
| `filter_field_id` | query | `string` | no | The ID of a form or hidden field to filter users by. |
| `filter_field_value` | query | `string` | no | The field value to pair with Filter Field ID when narrowing users. |
