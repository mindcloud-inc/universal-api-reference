# U-ON: List Payments

Retrieves payment records from U-ON within a date range.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-payments?connectionId=$CONNECTION_ID&date_from=2026-05-07T12%3A00%3A00.000Z&date_to=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date_from": "2026-05-07T12:00:00.000Z",
  "date_to": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-payments?${params}`, {
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
| `date_from` | date | yes | date_from path parameter |
| `date_to` | date | yes | date_to path parameter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cash_id": 1,
      "cio_id": 1,
      "client_id": 1,
      "currency_id": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "date_plan": "2026-05-07T12:00:00.000Z",
      "extended_fields": [
        "string"
      ],
      "form_id": 1,
      "from1c": 1,
      "id": 1,
      "is_bonus_pay": 1,
      "is_deposit": 1,
      "is_plan": 1,
      "koef": 1,
      "manager_id": 1,
      "manager_id_creator": 1,
      "note": "string",
      "number": "string",
      "office_id": 1,
      "other_type_id": 1,
      "parent_payment_id": 1,
      "prepay_id": 1,
      "price": 1,
      "r_id": 1,
      "reason": "string",
      "supplier_id": 1,
      "type_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cash_id` | number | Касса / Cash ID |
| `cio_id` | number | Вид платежа / Cash in-out type |
| `client_id` | number | Заказчик / Client ID |
| `currency_id` | number | Валюта / Currency ID |
| `date` | date | Дата платежа / Payment date |
| `date_plan` | date | Плановая дата платежа / Scheduled payment date |
| `extended_fields` | array | Дополнительные поля / Extended fields |
| `form_id` | number | Вид платежа / Payment form ID |
| `from1c` | number | Платеж из 1С / From 1C flag |
| `id` | number | ID платежа / Payment ID |
| `is_bonus_pay` | number | Оплата бонусами / Bonus payment flag |
| `is_deposit` | number | Депозитная операция / Deposit payment flag |
| `is_plan` | number | Плановый платеж / Scheduled payment flag |
| `koef` | number | Курс валюты / Currency rate |
| `manager_id` | number | Менеджер / Manager ID |
| `manager_id_creator` | number | Создавший менеджер / Creator manager ID |
| `note` | string | Примечание / Note |
| `number` | string | Номер платежа / Payment number |
| `office_id` | number | Офис / Office ID |
| `other_type_id` | number | Тип косвенного платежа / Other payment type ID |
| `parent_payment_id` | number | Родительский платеж / Parent payment ID |
| `prepay_id` | number | Тип предоплаты / Prepay type ID |
| `price` | number | Стоимость клиенту / Client price |
| `r_id` | number | ID заявки / Request ID |
| `reason` | string | Основание платежа / Payment reason |
| `supplier_id` | number | Партнер или туроператор / Supplier ID |
| `type_id` | number | Тип платежа / Payment type ID |

## Native endpoint

Through the native U-ON API, this operation is `GET /payment/list/{date_from}/{date_to}/{page}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

