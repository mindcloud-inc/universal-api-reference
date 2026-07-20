# Get Contact with Planfix

Retrieves a contact or company from Planfix.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact/:id`
- **Base URL:** `{accountBaseUrl}/rest`
- **Official documentation:** [Get Contact](https://help.planfix.com/restapidocs/#/Contact/get-contact-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Planfix contact identifier. |
| `fields` | query | `string` | no | Comma-delimited contact fields to return. |
