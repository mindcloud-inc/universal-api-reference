# List Translations with Phrase

Retrieves translations for a project from Phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/translations`
- **Base URL:** `https://api.phrase.com/v2`
- **Official documentation:** [List Translations](https://developers.phrase.com/en/api/strings/translations/list-all-translations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | Optional project branch name to scope translation results. |
| `order` | query | `string` | no | Optional sort direction such as asc or desc. |
| `project_id` | path | `string` | yes | Phrase project id whose translations should be listed. |
| `q` | query | `string` | no | Optional Phrase search query for translation content. |
| `sort` | query | `string` | no | Optional Phrase translation sort field such as key_name, created_at, or updated_at. |
