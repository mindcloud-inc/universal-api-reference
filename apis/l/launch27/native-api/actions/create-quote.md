# Create Quote with Launch27

Creates a new quote in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `quote`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Create Quote](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Quote requester first name. |
| `last_name` | body | `string` | yes | Quote requester last name. |
| `email` | body | `string` | yes | Quote requester email address. |
| `phone` | body | `string` | yes | Quote requester phone number. |
| `custom_fields` | body | `list<object>` | no | Optional Launch27 quote custom fields array. |
