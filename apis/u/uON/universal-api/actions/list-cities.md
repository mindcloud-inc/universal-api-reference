# U-ON: List Cities

Retrieves city records for a country in U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-cities?connectionId=$CONNECTION_ID&country_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-cities?${params}`, {
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
| `country_id` | number | yes | country_id path parameter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "name_en": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | ID / ID |
| `name` | string | Название / Name |
| `name_en` | string | Название латиницей / The name in Latin |

## Native endpoint

Through the native U-ON API, this operation is `GET /cities/{country_id}/{page}.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cities.md) for the provider-specific parameters and requirements.

