# Update User with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update User](https://everii-group.github.io/mocoapp-api-docs/sections/users.html#put-usersid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `active` | body | `string` | no |
| `avatar` | body | `string` | no |
| `bday` | body | `string` | no |
| `custom_properties` | body | `string` | no |
| `email` | body | `string` | no |
| `external` | body | `string` | no |
| `firstname` | body | `string` | no |
| `home_address` | body | `string` | no |
| `iban` | body | `string` | no |
| `id` | path | `number` | yes |
| `info` | body | `string` | no |
| `language` | body | `string` | no |
| `lastname` | body | `string` | no |
| `mobile_phone` | body | `string` | no |
| `password` | body | `string` | no |
| `role_id` | body | `string` | no |
| `tags` | body | `string` | no |
| `unit_id` | body | `string` | no |
| `welcome_email` | body | `string` | no |
| `work_phone` | body | `string` | no |
