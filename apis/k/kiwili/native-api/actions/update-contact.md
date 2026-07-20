# Update Contact with Kiwili

Updates an existing contact in Kiwili.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/:contact_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Update Contact](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The Kiwili contact ID to update. |
| `EnterpriseId` | body | `number` | no | The enterprise ID the contact belongs to. |
| `FirstName` | body | `string` | no | The updated contact first name. |
| `LastName` | body | `string` | no | The updated contact last name. |
