# Get Article By Path with Dev.to

Retrieves a published Dev.to article by username and slug path.

## Endpoint

- **Method:** `GET`
- **Path:** `/articles/:username/:slug`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [Get Article By Path](https://developers.forem.com/api/v1#tag/articles/operation/getArticleByPath)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Article author's username. |
| `slug` | path | `string` | yes | Article slug from the DEV path. |
