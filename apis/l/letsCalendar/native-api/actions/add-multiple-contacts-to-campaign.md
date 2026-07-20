# Add Multiple Contacts to Campaign with Let's Calendar

Adds multiple contacts to a campaign in Let's Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `add-contacts`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Add Multiple Contacts to Campaign](https://panel.letscalendar.com/docs#apis-POSTapi-lc-add-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
| `contacts[]` | body | `array<object>` | no | Array of contacts to add to the campaign. |
| `contacts[].firstname` | body | `string` | yes | The first name of the contact. |
| `contacts[].lastname` | body | `string` | no | The last name of the contact. |
| `contacts[].email` | body | `string` | yes | A valid email address. |
| `contacts[].loginurl` | body | `string` | no | The login URL for the contact. |
| `contacts[].username` | body | `string` | no | The username for the contact. |
| `contacts[].password` | body | `string` | no | The password for the contact. |
