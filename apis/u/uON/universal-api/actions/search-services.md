# U-ON: Search Services

Finds services in U-ON by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/search-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/search-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/search-services?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visa_docs_date_from_client_from` | date | no | Дата получения документов от клиента на визу (с даты), формат: Y-m-d / Date of visa docs from client (from), format: Y-m-d |
| `visa_docs_date_from_client_to` | date | no | Дата получения документов от клиента на визу (до даты), формат: Y-m-d / Date of visa docs from client (till), format: Y-m-d |
| `visa_docs_date_to_visa_center_from` | date | no | Дата сдачи документов в визовый центр (с даты), формат: Y-m-d / Date of visa docs to visa center (from), format: Y-m-d |
| `visa_docs_date_to_visa_center_to` | date | no | Дата сдачи документов в визовый центр (до даты), формат: Y-m-d / Date of visa docs to visa center (till), format: Y-m-d |
| `visa_docs_date_from_visa_center_from` | date | no | Дата получения документов из визового центра (с даты), формат: Y-m-d / Date of visa docs from visa center (from), format: Y-m-d |
| `visa_docs_date_from_visa_center_to` | date | no | Дата получения документов из визового центра (до даты), формат: Y-m-d / Date of visa docs from visa center (till), format: Y-m-d |
| `page` | number | no | Номер страницы выдачи (по-умолчанию, 1) / Page number (by default, 1) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city_id": 1,
      "country_id": 1,
      "course": "string",
      "date_begin": "2026-05-07T12:00:00.000Z",
      "date_end": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": "string",
      "hotel_id": 1,
      "hotel_place_id": 1,
      "hotel_type_id": 1,
      "id": 1,
      "in_package": 1,
      "nutrition_id": 1,
      "tourists_child_count": 1,
      "tourists_count": 1,
      "type_id": 1,
      "visa_docs_date_from_client": "2026-05-07T12:00:00.000Z",
      "visa_docs_date_from_visa_center": "2026-05-07T12:00:00.000Z",
      "visa_docs_date_to_visa_center": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city_id` | number | Курорт / City ID |
| `country_id` | number | Страна / Country ID |
| `course` | string | Маршрут / Route |
| `date_begin` | date | Дата начала услуги / Service start date |
| `date_end` | date | Дата окончания услуги / Service end date |
| `description` | string | Описание услуги / Service description |
| `duration` | string | Длительность / Duration |
| `hotel_id` | number | Отель / Hotel ID |
| `hotel_place_id` | number | Тип размещения / Hotel place ID |
| `hotel_type_id` | number | Тип номера / Hotel room type ID |
| `id` | number | ID услуги / Service ID |
| `in_package` | number | В составе пакета / In package flag |
| `nutrition_id` | number | Питание / Nutrition ID |
| `tourists_child_count` | number | Количество детей / Child tourist count |
| `tourists_count` | number | Количество взрослых туристов / Adult tourist count |
| `type_id` | number | Тип услуги / Service type ID |
| `visa_docs_date_from_client` | date | Дата получения документов от клиента / Visa docs from client date |
| `visa_docs_date_from_visa_center` | date | Дата получения документов из визового центра / Visa docs from visa center date |
| `visa_docs_date_to_visa_center` | date | Дата сдачи документов в визовый центр / Visa docs to visa center date |

## Native endpoint

Through the native U-ON API, this operation is `POST /service/search.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-services.md) for the provider-specific parameters and requirements.

