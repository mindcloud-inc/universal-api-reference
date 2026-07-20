# Batch Get Contact Groups with Google Contacts

Retrieves multiple contact groups from Google Contacts.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contactGroups\:batchGet`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Batch Get Contact Groups](https://developers.google.com/people/api/rest/v1/contactGroups/batchGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceNames` | query | `string` | yes | One contact group resource name. Use a single value for stable query serialization. |
| `groupFields` | query | `string` | no | Comma-separated ContactGroup fields to include. |
| `maxMembers` | query | `number` | no | Maximum members returned per contact group. |
