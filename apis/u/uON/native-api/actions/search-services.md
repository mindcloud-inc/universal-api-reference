# Search Services with U-ON

Finds services in U-ON by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/search.json`
- **Base URL:** `https://api.u-on.ru/{key}`
- **Official documentation:** [Search Services](https://api.u-on.travel/doc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `visa_docs_date_from_client_from` | body | `date` | no | Дата получения документов от клиента на визу (с даты), формат: Y-m-d / Date of visa docs from client (from), format: Y-m-d |
| `visa_docs_date_from_client_to` | body | `date` | no | Дата получения документов от клиента на визу (до даты), формат: Y-m-d / Date of visa docs from client (till), format: Y-m-d |
| `visa_docs_date_to_visa_center_from` | body | `date` | no | Дата сдачи документов в визовый центр (с даты), формат: Y-m-d / Date of visa docs to visa center (from), format: Y-m-d |
| `visa_docs_date_to_visa_center_to` | body | `date` | no | Дата сдачи документов в визовый центр (до даты), формат: Y-m-d / Date of visa docs to visa center (till), format: Y-m-d |
| `visa_docs_date_from_visa_center_from` | body | `date` | no | Дата получения документов из визового центра (с даты), формат: Y-m-d / Date of visa docs from visa center (from), format: Y-m-d |
| `visa_docs_date_from_visa_center_to` | body | `date` | no | Дата получения документов из визового центра (до даты), формат: Y-m-d / Date of visa docs from visa center (till), format: Y-m-d |
| `page` | body | `number` | no | Номер страницы выдачи (по-умолчанию, 1) / Page number (by default, 1) |
