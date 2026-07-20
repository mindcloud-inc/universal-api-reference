# Update Contact Property with SurveySparrow

Updates an existing contact property in SurveySparrow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contact_properties/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Update Contact Property](https://developers.surveysparrow.com/rest-apis/patch-v-3-contact-properties-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the contact property |
| `type` | body | `list` | no | Type of contact property |
| `label` | body | `string` | no | Label of the contact property |
| `description` | body | `string` | no | Description of the contact property |
| `contact_property_group_id` | body | `number` | no | Contact property group ID |
