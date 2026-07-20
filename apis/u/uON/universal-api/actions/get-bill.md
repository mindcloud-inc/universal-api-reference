# U-ON: Get Bill

Retrieves a bill record from U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-bill?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-bill?${params}`, {
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
      "cancelled_date": "2026-05-07T12:00:00.000Z",
      "client_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "hold_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_cancelled": 1,
      "is_hold": 1,
      "is_paid": 1,
      "manager_id": 1,
      "nds": "string",
      "note": "string",
      "number": "string",
      "paid_date": "2026-05-07T12:00:00.000Z",
      "paid_manager_id": 1,
      "price": 1,
      "r_id": 1,
      "reason": "string",
      "services": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled_date` | date | Дата отмены / Cancelled date |
| `client_id` | number | ID туриста (см.метод user) / Tourist ID (see method user) |
| `created_at` | date | Дата создания / Creation date |
| `date` | date | Дата / Date |
| `hold_date` | date | Дата холдирования / Hold date |
| `id` | number | ID / ID |
| `is_cancelled` | number | Отменен? / Is cancelled? |
| `is_hold` | number | На этапе холдирования? / Is hold? |
| `is_paid` | number | Оплачен? / Is paid? |
| `manager_id` | number | ID менеджера (см.метод manager) / Manager ID (see method manager) |
| `nds` | string | НДС / Nds |
| `note` | string | Примечание / Note |
| `number` | string | Номер / Number |
| `paid_date` | date | Дата оплаты / Paid date |
| `paid_manager_id` | number | Оплата проведена менеджером (списание холдированных средств) / Manager has completed hold |
| `price` | number | Сумма счета / Bill price |
| `r_id` | number | ID заявки / Request ID |
| `reason` | string | Назначение платежа / Bill reason |
| `services` | string | Список услуг внутри счета / Bill services |
| `url` | string | Ссылка на оплату / Link to pay |

## Native endpoint

Through the native U-ON API, this operation is `GET /bill/{id}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bill.md) for the provider-specific parameters and requirements.

