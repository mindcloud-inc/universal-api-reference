# Update Contact with NobelSMS

Updates an existing contact in NobelSMS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/:id`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Update Contact](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comments` | body | `string` | no | Comments. |
| `first_name` | body | `string` | no | First name. |
| `id` | path | `number` | yes | Contact ID. |
| `last_name` | body | `string` | no | Last name. |
| `phone` | body | `number` | no | Phone number. |
| `tag_ids` | body | `string` | no | Comma-separated list of tag IDs. |
