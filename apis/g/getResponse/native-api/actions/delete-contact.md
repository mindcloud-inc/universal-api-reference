# Delete Contact with GetResponse

Deletes a contact by ID from GetResponse.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Delete Contact](https://apireference.getresponse.com/#operation/deleteContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Unique identifier of the contact |
| `messageId` | query | `string` | no | Message ID to simulate unsubscribe flow |
| `ipAddress` | query | `string` | no | IP address used with messageId unsubscribe simulation |
