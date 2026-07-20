# Update Contact with Moco

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/people/:id`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [Update Contact](https://everii-group.github.io/mocoapp-api-docs/sections/contacts.html#put-contactspeopleid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `birthday` | body | `string` | no |
| `company_id` | body | `string` | no |
| `firstname` | body | `string` | no |
| `gender` | body | `string` | no |
| `home_address` | body | `string` | no |
| `home_email` | body | `string` | no |
| `id` | path | `number` | yes |
| `info` | body | `string` | no |
| `job_position` | body | `string` | no |
| `lastname` | body | `string` | no |
| `mobile_phone` | body | `string` | no |
| `tags` | body | `string` | no |
| `title` | body | `string` | no |
| `user_id` | body | `string` | no |
| `work_address` | body | `string` | no |
| `work_email` | body | `string` | no |
| `work_fax` | body | `string` | no |
| `work_phone` | body | `string` | no |
