# Delete Contact Group with Google Contacts

Deletes an existing contact group from Google Contacts.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/contactGroups/:resourceName`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Delete Contact Group](https://developers.google.com/people/api/rest/v1/contactGroups/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Contact group ID segment (for example, 4818b05f0a06bc27). |
| `deleteContacts` | query | `boolean` | no | If true, also delete member contacts when deleting the group. |
