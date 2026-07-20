# Update Contact with Close

Updates an existing contact in Close.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/:id/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Update Contact](https://developer.close.com/resources/contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique Contact ID. |
| `name` | body | `string` | no | Contact name. |
| `title` | body | `string` | no | Job title. |
