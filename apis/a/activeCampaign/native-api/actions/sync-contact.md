# Sync Contact with ActiveCampaign

Finds a contact in ActiveCampaign, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/sync`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Sync Contact](https://developers.activecampaign.com/reference/sync-a-contacts-data)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact` | body | `object` | no |
| `contact.email` | body | `string` | yes |
| `contact.firstName` | body | `string` | no |
| `contact.lastName` | body | `string` | no |
| `contact.phone` | body | `string` | no |
| `contact.fieldValues[]` | body | `array<object>` | no |
| `contact.deleted` | body | `boolean` | no |
