# Search Employees with Intradesk

Finds employees in Intradesk by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/api/v1/Employees/SearchHints`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Search Employees](https://apigw.intradesk.ru/settings_docs/swagger/index.html#/Employees/get_api_v1_Employees_SearchHints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchString` | query | `string` | no | Employee hint search text. |
| `top` | query | `number` | no | Maximum number of employee hints to return. |
| `excludedids[]` | query | `array<number>` | no | Employee IDs to exclude from hint results. Send multiple values as a array. |
