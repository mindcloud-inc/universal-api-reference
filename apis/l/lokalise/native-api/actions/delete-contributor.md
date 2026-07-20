# Delete Contributor with Lokalise

Deletes an existing contributor from Lokalise.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/contributors/:contributor_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Delete Contributor](https://developers.lokalise.com/reference/delete-a-contributor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contributor_id` | path | `string` | no | Lokalise contributor identifier. |
| `project_id` | path | `string` | no | Lokalise project identifier. |
