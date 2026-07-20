# Update Contact Group with Google Contacts

Updates an existing contact group in Google Contacts.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contactGroups/:resourceName`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Update Contact Group](https://developers.google.com/people/api/rest/v1/contactGroups/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Contact group ID segment (for example, 4818b05f0a06bc27). |
| `contactGroup.name` | body | `string` | yes | Updated contact group name. |
| `contactGroup.etag` | body | `string` | yes | Current ETag of the contact group. |
| `updateGroupFields` | body | `string` | yes | Comma-separated field mask of ContactGroup fields to update. |
| `readGroupFields` | body | `string` | no | Comma-separated fields to include in the updated group response. |
