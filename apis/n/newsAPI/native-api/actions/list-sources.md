# List Sources with News API

Retrieves top-headline news sources from News API.

## Endpoint

- **Method:** `GET`
- **Path:** `/top-headlines/sources`
- **Base URL:** `https://newsapi.org/v2`
- **Official documentation:** [List Sources](https://newsapi.org/docs/endpoints/sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Category of sources to return. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `language` | query | `string` | no | Language of sources to return. Accepted values: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `country` | query | `string` | no | Country of sources to return. Accepted values: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `20`, `21`, `22`, `23`, `24`, `25`, `26`, `27`, `28`, `29`, `3`, `30`, `31`, `32`, `33`, `34`, `35`, `36`, `37`, `38`, `39`, `4`, `40`, `41`, `42`, `43`, `44`, `45`, `46`, `47`, `48`, `49`, `5`, `50`, `51`, `52`, `53`, `6`, `7`, `8`, `9`. |
