# U-ON: Get Supplier

Retrieves a supplier record from U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-supplier?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-supplier?${params}`, {
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
      "address": "string",
      "bank_account": "string",
      "bik": "string",
      "contacts": "string",
      "director": "string",
      "director_position": "string",
      "director_position_rod": "string",
      "director_reason": "string",
      "director_rod": "string",
      "email": "ava@example.com",
      "ext_fields": [
        {}
      ],
      "id": 1,
      "inn": "string",
      "kpp": "string",
      "name": "Ava Chen",
      "name_official": "Ava Chen",
      "note": "string",
      "ogrn": "string",
      "phones": "string",
      "type": "string",
      "type_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Адрес партнера / The partner s address |
| `bank_account` | string | Банк и счет партнера / The partner bank account |
| `bik` | string | БИК банка партнера / The partner bank BIK |
| `contacts` | string | Контактная информация / Contact information |
| `director` | string | Директор партнера / The partner director |
| `director_position` | string | Должность директора партнера / The partner director position |
| `director_position_rod` | string | Должность директора партнера в родит.падеже / The partner director position rod |
| `director_reason` | string | На основе какого документа работает директор партнера / The partner director reason |
| `director_rod` | string | Директор партнера в родит.падеже / The partner director rod |
| `email` | string | E-mail партнера / E-mail partner |
| `ext_fields` | array<object> | Массив дополнительных полей и их значений в формате [ID поля1 => [значение, значение, ...], ID поля2 => [значение, значение, ...]] / Array of extended fields with values in format [ID field1 => [value, value, ...], ID field2 => [value, value, ...]] |
| `id` | number | ID партнера / ID |
| `inn` | string | ИНН партнера / The partner INN |
| `kpp` | string | КПП партнера / The partner KPP |
| `name` | string | Наименование партнера / The name of the partner |
| `name_official` | string | Официальное наименование партнера / Official name of the partner |
| `note` | string | Примечание / Note |
| `ogrn` | string | ОГРН партнера / The partner OGRN |
| `phones` | string | Телефоны партнера / Phones partner |
| `type` | string | Наименование типа / Type name |
| `type_id` | number | ID типа / Type ID |

## Native endpoint

Through the native U-ON API, this operation is `GET /supplier/{id}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

