# Add Tag To Contact with ActiveCampaign

Adds a tag to a contact in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/contactTags`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Add Tag To Contact](https://developers.activecampaign.com/reference/create-contact-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactTag` | body | `object` | no |
| `contactTag.contact` | body | `number` | no |
| `contactTag.tag` | body | `number` | no |
