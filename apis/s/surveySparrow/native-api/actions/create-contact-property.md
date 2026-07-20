# Create Contact Property with SurveySparrow

Creates a new contact property in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_properties`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Contact Property](https://developers.surveysparrow.com/rest-apis/post-v-3-contact-properties/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `list` | yes | Type of contact property |
| `label` | body | `string` | yes | Label of the contact property |
| `description` | body | `string` | no | Description of the contact property |
| `contact_property_group_id` | body | `number` | no | Contact property group ID |
