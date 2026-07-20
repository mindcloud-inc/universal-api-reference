# Update Organization with MailoPost

Updates an existing organization in MailoPost.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/organizations/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Update Organization](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost organization identifier. |
| `name` | body | `string` | no | Organization name. |
| `address` | body | `string` | no | Organization address. |
| `country` | body | `string` | no | Organization country. |
| `city` | body | `string` | no | Organization city. |
| `phone` | body | `string` | no | Organization phone number. |
| `zip` | body | `string` | no | Organization postal code. |
