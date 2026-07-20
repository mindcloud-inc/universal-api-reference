# Create Contact with SurveySparrow

Creates a new contact in SurveySparrow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [Create Contact](https://developers.surveysparrow.com/rest-apis/post-v-3-contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_name` | body | `string` | no | Full name of the contact. |
| `email` | body | `string` | yes | Email address of the contact. |
| `phone` | body | `string` | no | Phone number of the contact. |
| `mobile` | body | `string` | no | Mobile number of the contact. |
| `job_title` | body | `string` | no | Job title of the contact. |
| `contact_type` | body | `list` | no | Type of contact. Accepted values: `0`, `1`. |
| `referenceId` | body | `string` | no | Reference ID of the contact. |
| `unique_id` | body | `string` | no | Unique alphanumeric ID for the contact. |
| `unsubscribed` | body | `boolean` | no | Unsubscribed status of the contact. |
| `unsubscribe_text` | body | `string` | no | Reason for unsubscribing. |
