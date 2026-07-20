# List Articles with Helpjuice

Retrieves articles from Helpjuice.

## Endpoint

- **Method:** `GET`
- **Path:** `/articles`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Articles](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[accessibility]` | query | `number` | no | Filter articles by accessibility. 1 public, 0 internal, 2 private. |
| `filter[is_published]` | query | `boolean` | no | Filter articles by published state. |
| `created_since` | query | `string` | no | Only return articles created on or after this date in dd-mm-yyyy format. |
| `updated_since` | query | `string` | no | Only return articles updated on or after this date in dd-mm-yyyy format. |
| `filter[language]` | query | `string` | no | Filter articles by language shortcode such as en_us. |
