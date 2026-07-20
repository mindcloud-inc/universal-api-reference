# Get Contact Group with Google Contacts

Retrieves a contact group from Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contactGroups/:resourceName`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Get Contact Group](https://developers.google.com/people/api/rest/v1/contactGroups/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Contact group ID segment (for example, myContacts or 4818b05f0a06bc27). |
| `groupFields` | query | `string` | no | Comma-separated ContactGroup fields to include. |
| `maxMembers` | query | `number` | no | Maximum number of member resource names to include. |
