# List Content Categorizations with WebCategorize

## Endpoint

- **Method:** `GET`
- **Path:** `/html/get/all`
- **Base URL:** `https://app.webcategorize.com/api`
- **Official documentation:** [List Content Categorizations](https://webcategorize.com/webcategorize.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of records to return, from 1 to 1000. |
| `tag` | query | `string` | no | Matching tag. The API supports repeated tag query parameters. Send multiple values as a array. |
| `category` | query | `string` | no | Matching classification category. The API supports repeated category query parameters. Send multiple values as a array. |
| `language` | query | `string` | no | Matching language code. The API supports repeated language query parameters. Send multiple values as a array. |
| `url` | query | `string` | no | Partial URL match. |
