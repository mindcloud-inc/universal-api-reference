# Create Contact Group with HappyFox

Creates a new contact group in HappyFox.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_groups/`
- **Base URL:** `https://{accountDomain}/api/1.1/json`
- **Official documentation:** [Create Contact Group](https://support.happyfox.com/kb/article/1092-contacts-and-contact-groups-api-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact group name. |
| `description` | body | `string` | no | Optional contact group description. |
| `tagged_domains` | body | `string` | no | Optional domains to tag to the group. |
