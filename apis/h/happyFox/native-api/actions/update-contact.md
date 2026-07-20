# Update Contact with HappyFox

Updates an existing contact in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/:user_id/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Update Contact](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | HappyFox contact user ID. |
| `name` | body | `string` | no | Updated contact name. |
| `email` | body | `string` | no | Updated contact email address. |
