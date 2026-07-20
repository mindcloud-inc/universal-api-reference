# Update Contributor with Lokalise

Updates an existing contributor in Lokalise.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/contributors/:contributor_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Update Contributor](https://developers.lokalise.com/reference/update-a-contributor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contributor_id` | path | `string` | no | Lokalise contributor identifier. |
| `project_id` | path | `string` | no | Lokalise project identifier. |
