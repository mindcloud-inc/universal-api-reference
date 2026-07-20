# Update Person with Blueink

Updates an existing person in Blueink.

## Endpoint

- **Method:** `PUT`
- **Path:** `/persons/:personId/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Update Person](https://developer.blueink.com/api/#tag/Person/operation/updatePerson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | Person ID to update. |
| `name` | body | `string` | no | Updated name for the person. |
| `channels[].kind` | body | `string` | yes | Contact channel type. Use em for email. |
| `channels[].email` | body | `string` | yes | Email address for the contact channel. |
