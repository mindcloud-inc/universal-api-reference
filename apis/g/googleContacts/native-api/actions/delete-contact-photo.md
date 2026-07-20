# Delete Contact Photo with Google Contacts

Deletes a contact photo from Google Contacts.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/people/:resourceName:photoAction`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Delete Contact Photo](https://developers.google.com/people/api/rest/v1/people/deleteContactPhoto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | — |
| `personFields` | query | `string` | no | Optional person fields to include in returned person. |
| `sources` | query | `string` | no | Optional source types to include in returned person. |
