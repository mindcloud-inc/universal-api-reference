# Update Contact with ActiveCampaign

Updates an existing contact in ActiveCampaign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Update Contact](https://developers.activecampaign.com/reference/update-a-contact-new)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The contact ID. |
| `contact` | body | `object` | no | — |
| `contact.email` | body | `string` | no | — |
| `contact.firstName` | body | `string` | no | — |
| `contact.lastName` | body | `string` | no | — |
| `contact.phone` | body | `string` | no | — |
| `contact.fieldValues[]` | body | `array<object>` | no | — |
| `contact.deleted` | body | `boolean` | no | — |
