# U-ON: Get Hotel

Retrieves a hotel record from U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-hotel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-hotel?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/get-hotel?${params}`, {
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
      "bedroom_count": 1,
      "city": "string",
      "city_id": "string",
      "contacts": "string",
      "country": "string",
      "country_id": "string",
      "exit_hour": "string",
      "guests_count": 1,
      "id": 1,
      "name": "Ava Chen",
      "name_en": "Ava Chen",
      "notice": "string",
      "price": 1,
      "reserve_rules": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bedroom_count` | number | Количество спален / Number of bedrooms |
| `city` | string | Название города / The name of the city |
| `city_id` | string | ID города / ID of the city |
| `contacts` | string | Контактная информация / Contact information |
| `country` | string | Название страны / The name of the country |
| `country_id` | string | ID страны / ID of the country |
| `exit_hour` | string | Час выезда / Check out time |
| `guests_count` | number | Количество гостей / The number of guests |
| `id` | number | ID / ID |
| `name` | string | Название / Name |
| `name_en` | string | Название латиницей / The name in Latin |
| `notice` | string | Примечание / Note |
| `price` | number | Цена за 1 день / Price for 1 day |
| `reserve_rules` | string | Правила бронирования / Booking rules |
| `text` | string | Описание / Description |

## Native endpoint

Through the native U-ON API, this operation is `GET /hotel/{id}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hotel.md) for the provider-specific parameters and requirements.

