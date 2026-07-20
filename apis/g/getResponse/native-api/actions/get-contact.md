# Get Contact with GetResponse

Retrieves contact details by ID from GetResponse.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Get Contact](https://apireference.getresponse.com/#operation/getContactById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Unique identifier of the contact |
| `fields` | query | `string` | no | Comma-separated list of fields to return |
