# Create Client Contact with Jetbuilt

## Endpoint

- **Method:** `POST`
- **Path:** `clients/:client_id/contacts`
- **Base URL:** `https://app.jetbuilt.com/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `client_id` | path | `string` | no |
| `first_name` | body | `string` | no |
| `last_name` | body | `string` | no |
| `title` | body | `string` | no |
| `email_address` | body | `string` | no |
| `phone_number_1` | body | `string` | no |
| `phone_number_2` | body | `string` | no |
| `description` | body | `string` | no |
| `primary` | body | `boolean` | no |
