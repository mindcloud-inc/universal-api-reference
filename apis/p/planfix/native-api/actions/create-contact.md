# Create Contact with Planfix

Creates a new contact or company in Planfix.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Create Contact](https://help.planfix.com/restapidocs/#/Contact/post-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template.id` | body | `number` | yes | Contact template identifier. |
| `name` | body | `string` | yes | Contact or company name. |
| `email` | body | `string` | no | Primary email address. |
| `description` | body | `string` | no | Contact description. |
