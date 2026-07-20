# Find Contacts By Custom Field with Fliqr AI

## Endpoint

- **Method:** `GET`
- **Path:** `/users/find_by_custom_field`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Find Contacts By Custom Field](https://docs.fliqr.ai/api-reference/users/get-usersfind-by-custom-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_id` | query | `string` | yes | Custom field ID. Use phone or email to search those built-in fields. |
| `value` | query | `string` | yes | Custom field value to search for. |
