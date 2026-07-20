# Delete a contact from a specific group with Maildrip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/contacts/group/{group_id}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Delete a contact from a specific group](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | ID of the group from which the contact will be deleted |
| `contactId` | query | `string` | yes | ID of the contact to be deleted from the group |
