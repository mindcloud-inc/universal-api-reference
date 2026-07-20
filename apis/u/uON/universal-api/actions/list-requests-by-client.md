# U-ON: List Requests by Client

Retrieves request records for a U-ON client.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-requests-by-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-requests-by-client?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-requests-by-client?${params}`, {
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
| `id` | number | yes | id path parameter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calc_client": 1,
      "calc_decrease": 1,
      "calc_increase": 1,
      "calc_partner": 1,
      "calc_price": 1,
      "calc_price_netto": 1,
      "client_email": "ava@example.com",
      "client_id": 1,
      "client_name": "Ava Chen",
      "client_phone": "string",
      "client_sname": "Ava Chen",
      "client_surname": "Ava Chen",
      "dat": "2026-05-07T12:00:00.000Z",
      "dat_lead": "2026-05-07T12:00:00.000Z",
      "dat_updated": "2026-05-07T12:00:00.000Z",
      "date_begin": "2026-05-07T12:00:00.000Z",
      "date_end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "id_internal": "string",
      "id_system": "string",
      "manager_id": 1,
      "manager_name": "Ava Chen",
      "manager_sname": "Ava Chen",
      "manager_surname": "Ava Chen",
      "notes": "string",
      "services": {
        "city": "string",
        "city_en": "string",
        "city_id": 1,
        "country": "string",
        "country_en": "string",
        "country_id": 1,
        "currency": "string",
        "currency_code": "string",
        "currency_id": 1,
        "date_begin": "2026-05-07T12:00:00.000Z",
        "date_end": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "hotel": "string",
        "hotel_en": "string",
        "hotel_id": 1,
        "hotel_type": "string",
        "hotel_type_en": "string",
        "hotel_type_id": 1,
        "id": 1,
        "in_package": 1,
        "nutrition": "string",
        "nutrition_en": "string",
        "nutrition_id": 1,
        "partner": "string",
        "partner_en": "string",
        "partner_id": 1,
        "price": 1,
        "price_netto": 1,
        "rate": 1,
        "service_type": "string",
        "service_type_id": 1
      },
      "source": "string",
      "source_id": 1,
      "status": "string",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calc_client` | number | Сумма всех расчетов с клиентом / The sum of all payments to the client |
| `calc_decrease` | number | Сумма всех расходов / The amount of all expenses |
| `calc_increase` | number | Сумма всех приходов / The sum of all parishes |
| `calc_partner` | number | Сумма всех расчетов с партнерами / The sum of all payments |
| `calc_price` | number | Стоимость для клиента / The cost for the client |
| `calc_price_netto` | number | Себестоимость / The cost |
| `client_email` | string | E-mail клиента / E-mail client |
| `client_id` | number | ID клиента / Client ID |
| `client_name` | string | Имя клиента / The name of the customer |
| `client_phone` | string | Телефон клиента / Phone customer |
| `client_sname` | string | Отчество клиента / First name of client |
| `client_surname` | string | Фамилия клиента / The name of the client |
| `dat` | date | Дата создания заявки / Creation date of the application |
| `dat_lead` | date | Дата создания обращения (если заявка была создана из обращения) / Creation date of request (if the request was created out of circulation) |
| `dat_updated` | date | Дата последнего обновления заявки / Date of last update of the application |
| `date_begin` | date | Дата начала обслуживания / Start date of service |
| `date_end` | date | Дата окончания обслуживания / End date of service |
| `id` | string | ID / ID |
| `id_internal` | string | Внутренний номер / Internal number |
| `id_system` | string | Системный ID / System ID |
| `manager_id` | number | ID менеджера / ID Manager |
| `manager_name` | string | Имя менеджера / The name of the Manager |
| `manager_sname` | string | Отчество менеджера / The patronymic of the Manager |
| `manager_surname` | string | Фамилия менеджера / The name of the Manager |
| `notes` | string | Примечание / Note |
| `services.city` | string | Наименование города / The name of the city |
| `services.city_en` | string | Англ. наименование города / Eng. the name of the city |
| `services.city_id` | number | ID города / ID of the city |
| `services.country` | string | Наименование страны / The name of the country |
| `services.country_en` | string | Англ. наименование страны / Eng. the name of the country |
| `services.country_id` | number | ID страны / ID of the country |
| `services.currency` | string | Наименование валюты / The name of the currency |
| `services.currency_code` | string | Код валюты / Currency code |
| `services.currency_id` | number | ID валюты / The ID of the currency |
| `services.date_begin` | date | Дата начала услуги / Date of commencement of services |
| `services.date_end` | date | Дата окончания услуги / Date of completion of services |
| `services.description` | string | Описание услуги / Description of service |
| `services.hotel` | string | Наименование отеля / The name of the hotel |
| `services.hotel_en` | string | Англ. наименование отеля / Eng. the name of the hotel |
| `services.hotel_id` | number | ID отеля / ID of the hotel |
| `services.hotel_type` | string | Наименование типа номера / Name room type |
| `services.hotel_type_en` | string | Англ. наименование типа номера / Eng. name room type |
| `services.hotel_type_id` | number | ID типа номера / ID room type |
| `services.id` | number | ID услуги / ID services |
| `services.in_package` | number | В составе пакетного тура (1) или нет (0) / As part of a batch of tours (1) or not (0) |
| `services.nutrition` | string | Наименование питания / The name of the food |
| `services.nutrition_en` | string | Англ. наименование питания / Eng. the name of the food |
| `services.nutrition_id` | number | ID питания / ID nutrition |
| `services.partner` | string | Наименование партнера / The name of the partner |
| `services.partner_en` | string | Англ. наименование партнера / Eng. the name of the partner |
| `services.partner_id` | number | ID партнера / ID |
| `services.price` | number | Стоимость для клиента / The cost for the client |
| `services.price_netto` | number | Себестоимость услуги / The cost of services |
| `services.rate` | number | Курс валюты / Currency |
| `services.service_type` | string | Наименование типа услуги / The name of the service type |
| `services.service_type_id` | number | ID типа услуги / ID of the service type |
| `source` | string | Наименование источника / Source name |
| `source_id` | number | ID источника / Source ID |
| `status` | string | Наименование статуса / Name status |
| `status_id` | number | ID статуса / ID status |

## Native endpoint

Through the native U-ON API, this operation is `GET /request-by-client/{id}/{page}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-requests-by-client.md) for the provider-specific parameters and requirements.

