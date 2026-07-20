# Search Assets with Intradesk

Finds assets in Intradesk by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/api/v1/Assets/SearchHints`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Search Assets](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Assets/get_api_v1_Assets_SearchHints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchString` | query | `string` | no | Asset hint search text. |
| `top` | query | `number` | no | Maximum number of asset hints to return. |
| `excludedids[]` | query | `array<number>` | no | Asset IDs to exclude from hint results. Send multiple values as a array. |
