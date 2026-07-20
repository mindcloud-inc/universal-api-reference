# Create Contact with HappyFox

Creates a new contact in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Create Contact](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact name. |
| `email` | body | `string` | yes | Contact email address. |
