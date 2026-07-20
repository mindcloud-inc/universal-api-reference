# Update Contact List Status with ActiveCampaign

Updates a contact's list status in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/contactLists`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Update Contact List Status](https://developers.activecampaign.com/reference/update-list-status-for-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactList` | body | `object` | no |
| `contactList.list` | body | `string` | yes |
| `contactList.contact` | body | `string` | yes |
| `contactList.status` | body | `string` | yes |
| `contactList.sourceid` | body | `number` | no |
