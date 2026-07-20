# Add Single Contact to Campaign with Let's Calendar

Adds a contact to a campaign in Let's Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `add-single-contact`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Add Single Contact to Campaign](https://panel.letscalendar.com/docs#apis-POSTapi-lc-add-single-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
| `firstname` | body | `string` | yes | The first name of the contact. |
| `lastname` | body | `string` | no | The last name of the contact. |
| `email` | body | `string` | yes | A valid email address. |
| `loginurl` | body | `string` | no | The login URL for the contact. |
| `username` | body | `string` | no | The username for the contact. |
| `password` | body | `string` | no | The password for the contact. |
