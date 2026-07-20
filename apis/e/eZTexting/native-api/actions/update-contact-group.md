# Update Contact Group with EZ Texting

Updates a contact group in EZ Texting.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact-groups/:id`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Update Contact Group](https://developers.eztexting.com/reference/update_1-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact group ID |
| `name` | body | `string` | yes | Contact group name |
| `note` | body | `string` | no | Contact group note |
