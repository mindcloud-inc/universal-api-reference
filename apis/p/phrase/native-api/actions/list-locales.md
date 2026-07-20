# List Locales with Phrase

Retrieves locales for a project from Phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/locales`
- **Base URL:** `https://api.phrase.com/v2`
- **Official documentation:** [List Locales](https://developers.phrase.com/en/api/strings/locales/list-locales)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | Optional project branch name to scope locale results. |
| `project_id` | path | `string` | yes | Phrase project id whose locales should be listed. |
| `sort_by` | query | `string` | no | Optional Phrase locale sort order such as name_asc or default_desc. |
