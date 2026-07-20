# Create Contact with ActiveCampaign

Creates a new contact in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Create Contact](https://developers.activecampaign.com/reference/create-a-new-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact` | body | `object` | no |
| `contact.email` | body | `string` | no |
| `contact.allowNullEmail` | body | `boolean` | no |
| `contact.firstName` | body | `string` | no |
| `contact.lastName` | body | `string` | no |
| `contact.phone` | body | `string` | no |
| `contact.fieldValues[]` | body | `array<object>` | no |
