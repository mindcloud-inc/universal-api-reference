# Create Contact List with SurveySparrow

Creates a new contact list in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_lists`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Contact List](https://developers.surveysparrow.com/rest-apis/post-v-3-contact-lists/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the contact list. |
| `description` | body | `string` | no | Description of the contact list. |
