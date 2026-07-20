# Create Organization with MailoPost

Creates a new organization in MailoPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/organizations`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Create Organization](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Organization name. |
| `address` | body | `string` | yes | Organization address. |
| `country` | body | `string` | yes | Organization country. |
| `city` | body | `string` | yes | Organization city. |
| `phone` | body | `string` | yes | Organization phone number. |
| `zip` | body | `string` | yes | Organization postal code. |
