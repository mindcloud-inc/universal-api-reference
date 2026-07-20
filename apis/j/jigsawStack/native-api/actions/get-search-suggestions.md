# Get Search Suggestions with JigsawStack

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/web/search/suggest`
- **Base URL:** `https://api.jigsawstack.com`
- **Official documentation:** [Get Search Suggestions](https://jigsawstack.com/docs/api-reference/web/search-suggestions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The partial search phrase to autocomplete. Maximum length: 200. |
