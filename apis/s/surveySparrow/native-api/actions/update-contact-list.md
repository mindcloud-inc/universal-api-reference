# Update Contact List with SurveySparrow

Updates an existing contact list in SurveySparrow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contact_lists/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Update Contact List](https://developers.surveysparrow.com/rest-apis/patch-v-3-contact-lists-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the contact list |
| `name` | body | `string` | no | Name of the contact list |
| `description` | body | `string` | no | Description of the contact list |
