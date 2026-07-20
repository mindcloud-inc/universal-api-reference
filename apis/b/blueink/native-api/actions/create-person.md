# Create Person with Blueink

Creates a new person in Blueink.

## Endpoint

- **Method:** `POST`
- **Path:** `/persons/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Create Person](https://developer.blueink.com/api/#tag/Person/operation/createPerson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the person to create. |
| `channels[].kind` | body | `string` | yes | Contact channel type. Use em for email. |
| `channels[].email` | body | `string` | yes | Email address for the contact channel. |
