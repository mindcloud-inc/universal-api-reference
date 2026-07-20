# Create Contact with Campaign Refinery

Creates a new contact in Campaign Refinery.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/create-contact`
- **Base URL:** `https://app.campaignrefinery.com/rest`
- **Official documentation:** [Create Contact](https://developers.campaignrefinery.com/reference/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The contact's email address. |
| `first_name` | body | `string` | no | The contact's first name. |
| `last_name` | body | `string` | no | The contact's last name. |
