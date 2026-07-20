# Update Custom Field Value For Contact with ActiveCampaign

Updates a contact custom field value in ActiveCampaign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fieldValues/:id`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Update Custom Field Value For Contact](https://developers.activecampaign.com/reference/update-a-custom-field-value-for-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The field value ID. |
| `fieldValue` | body | `object` | no | — |
| `fieldValue.contact` | body | `string` | yes | — |
| `fieldValue.field` | body | `string` | yes | — |
| `fieldValue.value` | body | `string` | yes | — |
| `useDefaults` | body | `boolean` | no | — |
