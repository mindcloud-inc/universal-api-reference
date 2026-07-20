# Add Hiring Team Member with 100Hires ATS

Adds a hiring team member to a job in 100Hires ATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:id/hiring-team`
- **Base URL:** `https://api.100hires.com/v2`
- **Official documentation:** [Add Hiring Team Member](https://100hires.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Job ID or alias to add a hiring team member to. |
| `user_id` | body | `number` | yes | User ID to add to the hiring team. |
