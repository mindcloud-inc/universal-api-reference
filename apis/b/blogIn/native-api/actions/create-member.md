# Create Member with BlogIn

Creates a new member in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/members`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Create Member](https://blogin.co/api/rest/docs/#create-new-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address for the new member. |
| `username` | body | `string` | yes | The username for the new member. |
| `name` | body | `string` | no | The first name of the new member. |
| `surname` | body | `string` | no | The surname of the new member. |
| `access_level` | body | `string` | no | The access level of the new member. |
