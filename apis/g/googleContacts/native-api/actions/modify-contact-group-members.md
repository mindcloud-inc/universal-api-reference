# Modify Contact Group Members with Google Contacts

Updates contact group membership in Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contactGroups/:resourceName/members\:modify`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Modify Contact Group Members](https://developers.google.com/people/api/rest/v1/contactGroups.members/modify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | Contact group ID segment (for example, 4818b05f0a06bc27). |
| `resourceNamesToAdd[]` | body | `array<string>` | no | Person resource names to add to the group. |
| `resourceNamesToRemove[]` | body | `array<string>` | no | Person resource names to remove from the group. |
