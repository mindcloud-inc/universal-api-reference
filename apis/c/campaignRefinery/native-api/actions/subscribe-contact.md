# Subscribe Contact with Campaign Refinery

Subscribes an existing contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/subscribe`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Subscribe Contact](https://developers.campaignrefinery.com/reference/subscribe-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The contact's email address. |
| `first_name` | body | `string` | no | The contact's first name. |
| `last_name` | body | `string` | no | The contact's last name. |
| `tags` | body | `string` | no | One or more tag UUIDs separated by commas. Send multiple values as a string separated by `,`. |
| `sequences` | body | `string` | no | One or more sequence UUIDs separated by commas. Send multiple values as a string separated by `,`. |
| `form_id` | body | `string` | no | The form UUID to associate with the contact. |
| `goal_id` | body | `string` | no | The goal UUID to mark complete. |
