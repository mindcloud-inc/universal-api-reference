# Set Contact Custom Field with Fliqr AI

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user_id/custom_fields/:custom_field_id`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Set Contact Custom Field](https://docs.fliqr.ai/api-reference/users/post-users-custom-fields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Fliqr contact user ID. |
| `custom_field_id` | path | `string` | yes | Custom field ID. |
| `value` | body | `string` | yes | Value to set for the contact custom field. |
