# Create Text with DialMyCalls

Creates a new text in DialMyCalls.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/text`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Create Text](https://www.dialmycalls.com/api-documentation#text-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessaccount_id` | body | `string` | no | Schedule this broadcast as an access account. |
| `concatenate_sms` | body | `boolean` | no | Combine all SMS messages into one message on the end user's device. |
| `contacts[]` | body | `array<object>` | yes | List of contact information that should receive the broadcast. |
| `contacts[].email` | body | `string` | no | Contact email address. |
| `contacts[].firstname` | body | `string` | no | Contact first name. |
| `contacts[].lastname` | body | `string` | no | Contact last name. |
| `contacts[].phone` | body | `string` | yes | Contact phone number. |
| `keyword_id` | body | `string` | yes | The keyword ID that should be associated with this broadcast. |
| `messages[]` | body | `array<string>` | yes | List of messages to send, up to 10. |
| `name` | body | `string` | yes | Name the broadcast. |
| `send_at` | body | `string` | no | When the broadcast should be sent in UTC timestamp format like 2026-03-27T23:00:00+0000. |
| `send_email` | body | `boolean` | no | Also send an email to the contacts. |
| `send_immediately` | body | `boolean` | no | Whether the broadcast should go out immediately. |
| `shortcode_id` | body | `string` | no | The shortcode ID that the broadcast will be sent from. |
| `vanitynumber_id` | body | `string` | yes | The vanity number that the text broadcast will be sent from. |
