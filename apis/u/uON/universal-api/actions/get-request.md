# U-ON: Get Request

Retrieves a request record from U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-request?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-request?${params}`, {
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
      "bonus_limit": "string",
      "calc_client": 1,
      "calc_decrease": 1,
      "calc_increase": 1,
      "calc_partner": 1,
      "calc_price": 1,
      "calc_price_netto": 1,
      "client_company": "string",
      "client_email": "ava@example.com",
      "client_id": 1,
      "client_inn": "string",
      "client_kpp": "string",
      "client_name": "Ava Chen",
      "client_phone": "string",
      "client_phone_mobile": "string",
      "client_requirements_budget": "string",
      "client_requirements_country_ids": "string",
      "client_requirements_country_names": "Ava Chen",
      "client_requirements_date_from": "2026-05-07T12:00:00.000Z",
      "client_requirements_date_to": "2026-05-07T12:00:00.000Z",
      "client_requirements_days_from": "string",
      "client_requirements_days_to": "string",
      "client_requirements_hotel_stars": "string",
      "client_requirements_note": "string",
      "client_requirements_nutrition_ids": "string",
      "client_requirements_tourists_adult_count": "string",
      "client_requirements_tourists_baby_count": "string",
      "client_requirements_tourists_child_age": "string",
      "client_requirements_tourists_child_count": "string",
      "client_sname": "Ava Chen",
      "client_surname": "Ava Chen",
      "commission": "string",
      "company_fullname": "Ava Chen",
      "company_id": 1,
      "company_inn": "string",
      "company_name": "Ava Chen",
      "company_name_rus": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "dat": "2026-05-07T12:00:00.000Z",
      "dat_lead": "2026-05-07T12:00:00.000Z",
      "dat_request": "2026-05-07T12:00:00.000Z",
      "dat_updated": "2026-05-07T12:00:00.000Z",
      "date_begin": "2026-05-07T12:00:00.000Z",
      "date_close": "2026-05-07T12:00:00.000Z",
      "date_end": "2026-05-07T12:00:00.000Z",
      "extended_fields": [
        {}
      ],
      "files": "string",
      "id": "string",
      "id_internal": "string",
      "id_system": "string",
      "insurance_id": 1,
      "manager_id": 1,
      "manager_name": "Ava Chen",
      "manager_sname": "Ava Chen",
      "manager_surname": "Ava Chen",
      "max_payment_by_bonuses": 1,
      "max_payment_by_bonuses_in_percents": 1,
      "max_payment_by_bonuses_note": "string",
      "notes": "string",
      "office_id": 1,
      "payments": "string",
      "r_calc_client_currency_id": 1,
      "r_calc_partner_currency_id": 1,
      "r_created_u_id": 1,
      "reason_deny_id": 1,
      "reservation_number": "string",
      "roistat": "string",
      "services": "string",
      "source": "string",
      "source_id": 1,
      "status": "string",
      "status_id": 1,
      "supplier_id": 1,
      "supplier_inn": "string",
      "supplier_name": "Ava Chen",
      "tourists": "string",
      "travel_type": "string",
      "travel_type_id": 1,
      "utm_campaign": "string",
      "utm_content": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "utm_term": "string",
      "visa_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bonus_limit` | string | Лимит по оплате бонусами (в %) / Bonus payment limit (in %) |
| `calc_client` | number | Сумма всех расчетов с клиентом / The sum of all payments to the client |
| `calc_decrease` | number | Сумма всех расходов / The amount of all expenses |
| `calc_increase` | number | Сумма всех приходов / The sum of all parishes |
| `calc_partner` | number | Сумма всех расчетов с партнерами / The sum of all payments |
| `calc_price` | number | Стоимость для клиента / The cost for the client |
| `calc_price_netto` | number | Себестоимость / The cost |
| `client_company` | string | Компания клиента / Client company |
| `client_email` | string | E-mail клиента / E-mail client |
| `client_id` | number | ID клиента / Client ID |
| `client_inn` | string | ИНН клиента / Client INN |
| `client_kpp` | string | КПП клиента / Client KPP |
| `client_name` | string | Имя клиента / The name of the customer |
| `client_phone` | string | Телефон клиента / Phone customer |
| `client_phone_mobile` | string | Телефон клиента мобильный / Mobile phone customer |
| `client_requirements_budget` | string | Пожелания клиента в обращении: бюджет / Client's wishes: budget |
| `client_requirements_country_ids` | string | Пожелания клиента в обращении: ID стран / Client's wishes: countries IDs |
| `client_requirements_country_names` | string | Пожелания клиента в обращении: Названия стран / Client's wishes: countries names |
| `client_requirements_date_from` | date | Пожелания клиента в обращении: дата ОТ / Client's wishes: from date |
| `client_requirements_date_to` | date | Пожелания клиента в обращении: дата ДО / Client's wishes: to date |
| `client_requirements_days_from` | string | Пожелания клиента в обращении: количество дней ОТ / Client's wishes: days count from |
| `client_requirements_days_to` | string | Пожелания клиента в обращении: количество дней ДО / Client's wishes: days count to |
| `client_requirements_hotel_stars` | string | Пожелания клиента в обращении: количество звезд отеля / Client's wishes: hotel stars |
| `client_requirements_note` | string | Пожелания клиента в обращении: примечание / Client's wishes: note |
| `client_requirements_nutrition_ids` | string | Пожелания клиента в обращении: ID типов питания / Client's wishes: nutrition IDs |
| `client_requirements_tourists_adult_count` | string | Пожелания клиента в обращении: количество взрослых туристов / Client's wishes: adult tourists count |
| `client_requirements_tourists_baby_count` | string | Пожелания клиента в обращении: количество туристов младенцев / Client's wishes: baby tourists count |
| `client_requirements_tourists_child_age` | string | Пожелания клиента в обращении: возраст туристов-детей / Client's wishes: child tourists ages |
| `client_requirements_tourists_child_count` | string | Пожелания клиента в обращении: количество туристов детей / Client's wishes: child tourists count |
| `client_sname` | string | Отчество клиента / First name of client |
| `client_surname` | string | Фамилия клиента / The name of the client |
| `commission` | string | Массив комиссий по платежам (см.метод /payment/create) / An array of commission payments (see method /payment/create) |
| `company_fullname` | string | Полное название оформляющей компании / Company full name |
| `company_id` | number | ID оформляющей компании (ваше юрлицо) / Company ID |
| `company_inn` | string | ИНН оформляющей компании / Company INN |
| `company_name` | string | Название оформляющей компании / Company name |
| `company_name_rus` | string | Русское название оформляющей компании / Company name RUS |
| `created_at` | date | Дата создания (неизменяемая) / Created date (not edited) |
| `dat` | date | Дата создания записи в базе / Created date |
| `dat_lead` | date | Дата создания именно обращения / Created date of lead |
| `dat_request` | date | Дата создания именно заявки / Created date of request |
| `dat_updated` | date | Дата обновления / Updated date |
| `date_begin` | date | Дата начала обслуживания / Start date of service |
| `date_close` | date | Дата закрытия заявки / Close date of request |
| `date_end` | date | Дата окончания обслуживания / End date of service |
| `extended_fields` | array<object> | Массив значений дополнительных полей в виде [ID доп.поля => значение, ID доп.поля2 => значение2, ...] (см.метод /extended_field) / Array of values for extended fields [ID field => value, ID field2 => value2, ...] (see method /extended_field) |
| `files` | string | Массив прикрепленных файлов (см.метод /request_file/create) / An array of attached files (see method /request_file/create) |
| `id` | string | ID / ID |
| `id_internal` | string | Внутренний номер / Internal number |
| `id_system` | string | Системный ID / System ID |
| `insurance_id` | number | ID поля страховки / ID insurance |
| `manager_id` | number | ID прикрепленного менеджера / ID Manager |
| `manager_name` | string | Имя менеджера / The name of the Manager |
| `manager_sname` | string | Отчество менеджера / The patronymic of the Manager |
| `manager_surname` | string | Фамилия менеджера / The name of the Manager |
| `max_payment_by_bonuses` | number | Максимальная сумма оплаты заявки бонусами (в деньгах) / Max payment of request by bonuses (in money) |
| `max_payment_by_bonuses_in_percents` | number | Максимальная сумма оплаты заявки бонусами (в процентах) / Max payment of request by bonuses (in percents) |
| `max_payment_by_bonuses_note` | string | Максимальная сумма оплаты заявки бонусами (расчет) / Max payment of request by bonuses (calc) |
| `notes` | string | Примечание / Note |
| `office_id` | number | ID прикрепленного офиса / ID office |
| `payments` | string | Массив платежей (см.метод /payment/create) / An array of payments (see method /payment/create) |
| `r_calc_client_currency_id` | number | ID валюты расчетов с партнерами / Currency ID for clients finance |
| `r_calc_partner_currency_id` | number | ID валюты расчетов с партнерами / Currency ID for partners finance |
| `r_created_u_id` | number | ID менеджера, создавшего заявку / Manager ID, who created request |
| `reason_deny_id` | number | ID причины отказа в обращении / ID reason deny in lead |
| `reservation_number` | string | Номер брони / Reservation number |
| `roistat` | string | roistat |
| `services` | string | Массив услуг (см.метод /service) / An array of services (see method /service) |
| `source` | string | Наименование источника / Source name |
| `source_id` | number | ID источника / Source ID |
| `status` | string | Наименование статуса / Name status |
| `status_id` | number | ID статуса / ID status |
| `supplier_id` | number | ID туроператора / ID tour operator |
| `supplier_inn` | string | ИНН туроператора / Tour operator INN |
| `supplier_name` | string | Наименование туроператора / The name of the tour operator |
| `tourists` | string | Массив туристов (см.метод /user) / An array of tourists (see method /user) |
| `travel_type` | string | Наименование типа тура / Type name of the tour |
| `travel_type_id` | number | ID типа тура / Type ID of the tour |
| `utm_campaign` | string | utm_campaign |
| `utm_content` | string | utm_content |
| `utm_medium` | string | utm_medium |
| `utm_source` | string | utm_source |
| `utm_term` | string | utm_term |
| `visa_id` | number | ID поля визы / ID visa |

## Native endpoint

Through the native U-ON API, this operation is `GET /request/{id}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request.md) for the provider-specific parameters and requirements.

