# Create Person with folk

Creates a new person in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Person](https://developer.folk.app/api-reference/people/create-a-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fullName` | body | `string` | yes | The full name of the person. |
| `description` | body | `string` | no | A short description for the person. |
| `jobTitle` | body | `string` | no | The person's job title. |
