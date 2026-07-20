# Create Contact with ProProfs Project

Creates a new contact in ProProfs Project.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Create Contact](https://help.proprofsproject.com/managing-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `string` | no | Associate the contact with a client. |
| `contact_name` | body | `string` | yes | The contact name. |
| `email` | body | `string` | no | The contact email. |
