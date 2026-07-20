# Search Articles with HelpDocs

Finds articles in HelpDocs by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Search Articles](https://apidocs.helpdocs.io/article/If1U9NNUpT-searching-for-articles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search term. |
| `limit` | query | `number` | no | Maximum results to return. |
| `include_draft` | query | `boolean` | no | Include draft articles in the results. |
| `include_private` | query | `boolean` | no | Include private articles in the results. |
| `language_code` | query | `string` | no | Restrict search to a language code. |
