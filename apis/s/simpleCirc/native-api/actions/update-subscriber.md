# Update Subscriber with SimpleCirc

Updates an existing subscriber in SimpleCirc.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1.2/subscribers/:account_id`
- **Base URL:** `https://simplecirc.com`
- **Official documentation:** [Update Subscriber](https://simplecirc.com/docs/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `name` | body | `string` | no |
| `email` | body | `string` | no |
| `company` | body | `string` | no |
| `phone` | body | `string` | no |
| `title` | body | `string` | no |
| `custom_fields` | body | `object` | no |
