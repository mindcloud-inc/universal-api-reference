# Create or Update Team Member with Simplesat

Creates or updates a team member in Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/team-members`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Create or Update Team Member](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `external_id` | body | `string` | no |
| `name` | body | `string` | no |
| `email` | body | `string` | no |
| `custom_attributes` | body | `object` | no |
