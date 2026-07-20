# Request Person Deletion with Rollbar

Creates a person deletion request in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/delete_jobs/`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Request Person Deletion](https://docs.rollbar.com/reference/request-person-deletion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Tracked person email address |
| `person_id` | body | `string` | no | Tracked person identifier |
| `username` | body | `string` | no | Tracked person username |
