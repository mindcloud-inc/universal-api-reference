# List Contact Groups with Google Contacts

Retrieves contact groups from Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contactGroups`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [List Contact Groups](https://developers.google.com/people/api/rest/v1/contactGroups/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupFields` | query | `string` | no | Comma-separated ContactGroup fields to include. |
| `pageSize` | query | `number` | no | Maximum number of groups to return. |
| `pageToken` | query | `string` | no | Token from a previous page. |
| `syncToken` | query | `string` | no | Sync token from prior full sync. |
