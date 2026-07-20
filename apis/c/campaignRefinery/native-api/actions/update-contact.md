# Update Contact with Campaign Refinery

Updates an existing contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/update-contact`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Update Contact](https://developers.campaignrefinery.com/reference/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The contact's ID. |
| `first_name` | body | `string` | no | The contact's first name. |
| `last_name` | body | `string` | no | The contact's last name. |
| `email` | body | `string` | no | The contact's email address. |
