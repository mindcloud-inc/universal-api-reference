# Create Custom Field Value with ActiveCampaign

Creates a custom field value in ActiveCampaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/fieldValues`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [Create Custom Field Value](https://developers.activecampaign.com/reference/create-fieldvalue)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fieldValue` | body | `object` | no |
| `fieldValue.contact` | body | `string` | yes |
| `fieldValue.field` | body | `string` | yes |
| `fieldValue.value` | body | `string` | yes |
| `useDefaults` | body | `boolean` | no |
