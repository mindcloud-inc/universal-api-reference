# List Comments with Moco

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://{domain}.mocoapp.com/api/v1`
- **Official documentation:** [List Comments](https://everii-group.github.io/mocoapp-api-docs/sections/comments.html#get-comments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `commentable_id` | query | `number` | no |
| `commentable_type` | query | `string` | no |
| `custom_properties` | query | `object` | no |
| `ids` | query | `string` | no |
| `manual` | query | `boolean` | no |
| `updated_after` | query | `date` | no |
| `user_id` | query | `number` | no |
