# List Keys with Phrase

Retrieves translation keys for a project from Phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/keys`
- **Base URL:** `https://api.phrase.com/v2`
- **Official documentation:** [List Keys](https://developers.phrase.com/en/api/strings/keys/list-keys)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | query | `string` | no | Optional project branch name to scope key results. |
| `locale_id` | query | `string` | no | Optional locale id used for translated or untranslated key filters. |
| `order` | query | `string` | no | Optional sort direction such as asc or desc. |
| `project_id` | path | `string` | yes | Phrase project id whose keys should be listed. |
| `q` | query | `string` | no | Optional Phrase search query for key names and supported qualifiers. |
| `sort` | query | `string` | no | Optional Phrase key sort field such as name, created_at, or updated_at. |
