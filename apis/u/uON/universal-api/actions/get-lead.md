# U-ON: Get Lead

Retrieves a lead record from U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-lead?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-lead?${params}`, {
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
      "date_begin": "2026-05-07T12:00:00.000Z",
      "date_end": "2026-05-07T12:00:00.000Z",
      "extended_fields": [
        {}
      ],
      "files": "string",
      "id": "string",
      "id_internal": "string",
      "id_system": "string",
      "manager_id": 1,
      "manager_name": "Ava Chen",
      "manager_sname": "Ava Chen",
      "manager_surname": "Ava Chen",
      "notes": "string",
      "services": "string",
      "source": "string",
      "source_id": 1,
      "status": "string",
      "status_id": 1,
      "tours": "string"
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
| `dat` | date | Дата создания / Created date |
| `date_begin` | date | Дата начала обслуживания / Start date of service |
| `date_end` | date | Дата окончания обслуживания / End date of service |
| `extended_fields` | array<object> | Массив значений дополнительных полей в виде [ID доп.поля => значение, ID доп.поля2 => значение2, ...] (см.метод /extended_field) / Array of values for extended fields [ID field => value, ID field2 => value2, ...] (see method /extended_field) |
| `files` | string | Массив прикрепленных файлов (см.метод /request_file/create) / An array of attached files (see method /request_file/create) |
| `id` | string | ID / ID |
| `id_internal` | string | Внутренний номер / Internal number |
| `id_system` | string | Системный ID / System ID |
| `manager_id` | number | ID менеджера / ID Manager |
| `manager_name` | string | Имя менеджера / The name of the Manager |
| `manager_sname` | string | Отчество менеджера / The patronymic of the Manager |
| `manager_surname` | string | Фамилия менеджера / The name of the Manager |
| `notes` | string | Примечание / Note |
| `services` | string | Массив услуг (см.метод /service) / An array of services (see method /service) |
| `source` | string | Наименование источника / Source name |
| `source_id` | number | ID источника / Source ID |
| `status` | string | Наименование статуса / Name status |
| `status_id` | number | ID статуса / ID status |
| `tours` | string | Массив подборок туров / An array of tours |

## Native endpoint

Through the native U-ON API, this operation is `GET /lead/{id}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

