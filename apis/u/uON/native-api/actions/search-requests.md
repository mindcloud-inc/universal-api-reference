# Search Requests with U-ON

Finds requests in U-ON by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/request/search.json`
- **Base URL:** `https://api.u-on.ru/{key}`
- **Official documentation:** [Search Requests](https://api.u-on.travel/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_lead_create_from` | body | `date` | no | Дата создания обращения (от), формат YYYY-mm-dd HH:ii / Create date of request (from) |
| `date_lead_create_to` | body | `date` | no | Дата создания обращения (до), формат YYYY-mm-dd HH:ii / Create date of request (till) |
| `date_create_from` | body | `date` | no | Дата создания заявки (от), формат YYYY-mm-dd HH:ii / Create date of request (from) |
| `date_create_to` | body | `date` | no | Дата создания заявки (до), формат YYYY-mm-dd HH:ii / Create date of request (till) |
| `date_begin_from` | body | `date` | no | Дата начала заявки (от), формат YYYY-mm-dd HH:ii / Start date of request (from) |
| `date_begin_to` | body | `date` | no | Дата начала заявки (до), формат YYYY-mm-dd HH:ii / Start date of request (till) |
| `date_end_from` | body | `date` | no | Дата окончания заявки (от), формат YYYY-mm-dd HH:ii / End date of request (from) |
| `date_end_to` | body | `date` | no | Дата окончания заявки (до), формат YYYY-mm-dd HH:ii / End date of request (till) |
| `r_id_system` | body | `string` | no | Системный ID заявки / Request's system ID |
| `r_id_internal` | body | `string` | no | Внутренний ID заявки / Request's internal ID |
| `reservation_number` | body | `string` | no | Номер брони / Request's reservation number |
| `office_ids` | body | `string` | no | ID офисов (через запятую) / Office IDs (delimited by comma) |
| `manager_ids` | body | `string` | no | ID менеджеров (через запятую) / Manager IDs (delimited by comma) |
| `client_ids` | body | `string` | no | ID клиентов (через запятую) / Client IDs (delimited by comma) |
| `tourist_ids` | body | `string` | no | ID туристов (через запятую) / Tourist IDs (delimited by comma) |
| `source_ids` | body | `string` | no | ID источников (через запятую) / Source IDs (delimited by comma) |
| `type_ids` | body | `string` | no | ID типов заявок (через запятую) / Request type IDs (delimited by comma) |
| `status_ids` | body | `string` | no | ID статусов (через запятую) / Status IDs (delimited by comma) |
| `pay_status_ids` | body | `string` | no | ID статусов по оплате (через запятую) / Pay status IDs (delimited by comma) |
| `service_type_ids` | body | `string` | no | ID типов услуг внутри заявки (через запятую) / Service type IDs inside request (delimited by comma) |
| `ext_fields[]` | body | `array<string>` | no | Массив дополнительных полей и их значений в формате [ID поля1 => [значение, значение, ...], ID поля2 => [значение, значение, ...]] / Array of extended fields with values in format [ID field1 => [value, value, ...], ID field2 => [value, value, ...]] |
| `calc_price_from` | body | `number` | no | Стоимость для клиента (от) / The cost for the client (from) |
| `calc_price_to` | body | `number` | no | Стоимость для клиента (до) / The cost for the client (till) |
| `calc_price_netto_from` | body | `number` | no | Себестоимость для клиента (от) / Netto cost for the client (from) |
| `calc_price_netto_to` | body | `number` | no | Себестоимость для клиента (до) / Netto cost for the client (till) |
| `calc_client_from` | body | `number` | no | Оплаты клиента (от) / Client payments (from) |
| `calc_client_to` | body | `number` | no | Оплаты клиента (до) / Client payments (till) |
| `calc_partner_from` | body | `number` | no | Оплаты партнерам (от) / Partner payments (from) |
| `calc_partner_to` | body | `number` | no | Оплаты партнерам (до) / Partner payments (till) |
| `page` | body | `number` | no | Номер страницы выдачи (по-умолчанию, 1) / Page number (by default, 1) |
