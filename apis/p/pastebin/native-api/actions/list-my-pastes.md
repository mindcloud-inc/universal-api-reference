# List My Pastes with Pastebin

Retrieves pastes created by the current Pastebin user.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_post.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [List My Pastes](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_results_limit` | body | `string` | no | Optional number of pastes to return. Pastebin defaults to 50 and allows up to 1000. |
