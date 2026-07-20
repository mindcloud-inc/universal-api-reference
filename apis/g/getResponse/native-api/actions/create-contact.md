# Create Contact with GetResponse

Creates a new contact in GetResponse.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Create Contact](https://apireference.getresponse.com/#operation/createContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address |
| `campaign.campaignId` | body | `string` | yes | Campaign ID for the contact |
| `name` | body | `string` | no | Contact name |
| `dayOfCycle` | body | `string` | no | Autoresponder cycle day |
| `note` | body | `string` | no | Internal note for the contact |
