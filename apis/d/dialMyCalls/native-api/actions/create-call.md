# Create Call with DialMyCalls

Creates a new call in DialMyCalls.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/call`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Create Call](https://www.dialmycalls.com/api-documentation#call-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessaccount_id` | body | `string` | no | Schedule this broadcast as an access account. |
| `callerid_id` | body | `string` | yes | The caller ID that the message should be sent from. |
| `contacts[]` | body | `array<object>` | yes | List of contact information that should receive the broadcast. |
| `contacts[].email` | body | `string` | no | Contact email address. |
| `contacts[].firstname` | body | `string` | no | Contact first name. |
| `contacts[].lastname` | body | `string` | no | Contact last name. |
| `contacts[].phone` | body | `string` | yes | Contact phone number. |
| `machine_recording_id` | body | `string` | no | The recording ID to play on answering machines. |
| `name` | body | `string` | yes | Name the broadcast. |
| `recording_id` | body | `string` | yes | The recording ID of the message that should be played. |
| `send_at` | body | `string` | no | When the broadcast should be sent in UTC timestamp format like 2026-03-27T23:00:00+0000. |
| `send_email` | body | `boolean` | no | Also send an email to the contacts. |
| `send_immediately` | body | `boolean` | no | Whether the broadcast should go out immediately. |
| `use_amd` | body | `boolean` | no | Whether to use answering machine detection. |
