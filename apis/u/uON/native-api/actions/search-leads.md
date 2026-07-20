# Search Leads with U-ON

Finds leads in U-ON by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/search.json`
- **Base URL:** `https://api.u-on.ru/{key}`
- **Official documentation:** [Search Leads](https://api.u-on.travel/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_create_from` | body | `date` | no | Дата создания заявки (от) / Create date of request (from) |
| `date_create_to` | body | `date` | no | Дата создания заявки (до) / Create date of request (till) |
| `office_ids` | body | `string` | no | ID офисов (через запятую) / Office IDs (delimited by comma) |
| `manager_ids` | body | `string` | no | ID менеджеров (через запятую) / Manager IDs (delimited by comma) |
| `client_ids` | body | `string` | no | ID клиентов (через запятую) / Client IDs (delimited by comma) |
| `source_ids` | body | `string` | no | ID источников (через запятую) / Source IDs (delimited by comma) |
| `type_ids` | body | `string` | no | ID типов обращений (через запятую) / Source IDs (delimited by comma) |
| `status_ids` | body | `string` | no | ID статусов (через запятую) / Status IDs (delimited by comma) |
| `extended_fields[]` | body | `array<string>` | no | Массив дополнительных полей и их значений в формате [ID поля1 => [значение, значение, ...], ID поля2 => [значение, значение, ...]] / Array of extended fields with values in format [ID field1 => [value, value, ...], ID field2 => [value, value, ...]] |
| `page` | body | `number` | no | Номер страницы выдачи (по-умолчанию, 1) / Page number (by default, 1) |
