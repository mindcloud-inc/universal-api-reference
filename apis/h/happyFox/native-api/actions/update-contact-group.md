# Update Contact Group with HappyFox

Updates an existing contact group in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_group/:contact_group_id/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Update Contact Group](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_group_id` | path | `string` | yes | HappyFox contact group ID. |
| `description` | body | `string` | no | Updated contact group description. |
| `tagged_domains` | body | `string` | no | Updated domains tagged to the group. |
