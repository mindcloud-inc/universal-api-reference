# Create Team with Rollbar

Creates a new team in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Create Team](https://docs.rollbar.com/reference/create-a-team)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_level` | body | `string` | yes | Team access level. |
| `name` | body | `string` | yes | Name of the team. |
