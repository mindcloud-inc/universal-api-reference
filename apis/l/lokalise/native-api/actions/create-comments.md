# Create Comments with Lokalise

Creates comments for a Lokalise key.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/keys/:key_id/comments`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Create Comments](https://developers.lokalise.com/reference/create-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Lokalise project identifier. |
| `key_id` | path | `string` | yes | Lokalise key identifier. |
| `comments` | body | `string<string>` | yes | List of comment strings to add to the key. Send multiple values as a array. |
