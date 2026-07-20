# Update Person with folk

Updates an existing person in folk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/people/:personId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Update Person](https://developer.folk.app/api-reference/people/update-a-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | The ID of the person to update. |
| `fullName` | body | `string` | no | The updated full name of the person. |
| `description` | body | `string` | no | The updated description for the person. |
| `jobTitle` | body | `string` | no | The updated job title for the person. |
