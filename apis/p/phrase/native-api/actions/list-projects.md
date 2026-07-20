# List Projects with Phrase

Retrieves a list of projects from Phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.phrase.com/v2`
- **Official documentation:** [List Projects](https://developers.phrase.com/en/api/strings/projects/list-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | query | `string` | no | Optional Phrase account id to scope returned projects. |
| `sort_by` | query | `string` | no | Optional Phrase project sort order such as name_asc or updated_at_desc. |
