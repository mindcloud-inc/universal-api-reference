# Create Contact with NobelSMS

Creates a new contact in NobelSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact`
- **Base URL:** `https://api.nobelsms.com/rest`
- **Official documentation:** [Create Contact](https://api.nobelsms.com/rest/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comments` | body | `string` | no | Comments. |
| `first_name` | body | `string` | no | First name. |
| `last_name` | body | `string` | no | Last name. |
| `phone` | body | `number` | yes | Phone number. |
| `tag_ids` | body | `string` | yes | Comma-separated list of tag IDs. |
