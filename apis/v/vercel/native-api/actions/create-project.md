# Create Project with Vercel

Creates a new project in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v11/projects`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Create Project](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/create-a-new-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The desired name for the project |
