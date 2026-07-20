# Update Contact with GetResponse

Updates an existing contact in GetResponse.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Update Contact](https://apireference.getresponse.com/#operation/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Unique identifier of the contact |
| `email` | body | `string` | no | Contact email address |
| `campaign.campaignId` | body | `string` | no | Campaign ID for the contact |
| `name` | body | `string` | no | Contact name |
| `dayOfCycle` | body | `string` | no | Autoresponder cycle day |
| `note` | body | `string` | no | Internal note for the contact |
| `scoring` | body | `number` | no | Contact scoring value |
