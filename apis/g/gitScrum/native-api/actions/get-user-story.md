# Get User Story with GitScrum

Retrieves a specific GitScrum user story.

## Endpoint

- **Method:** `GET`
- **Path:** `/user-stories/:slug`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Get User Story](https://docs.gitscrum.com/en/api/user-stories)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `company_slug` | query | `string` | no |
| `project_slug` | query | `string` | no |
| `slug` | path | `string` | no |
