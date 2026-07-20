# Update Contact with SurveySparrow

Updates an existing contact in SurveySparrow.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/{{id}}`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Update Contact](https://developers.surveysparrow.com/rest-apis/put-v-3-contacts-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the contact. |
| `full_name` | body | `string` | no | Full name of the contact. |
| `email` | body | `string` | no | Email address of the contact. |
| `phone` | body | `string` | no | Phone number of the contact. |
| `mobile` | body | `string` | no | Mobile number of the contact. |
| `job_title` | body | `string` | no | Job title of the contact. |
| `referenceId` | body | `string` | no | Reference ID of the contact. |
| `unique_id` | body | `string` | no | Unique alphanumeric ID for the contact. |
| `unsubscribe_text` | body | `string` | no | Reason for unsubscribing. |
