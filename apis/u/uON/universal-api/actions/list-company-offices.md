# U-ON: List Company Offices

Retrieves company office records stored in U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-company-offices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-company-offices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-company-offices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "id": 1,
      "name": "Ava Chen",
      "phones": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Адрес / Address |
| `city` | string | Город / City |
| `id` | number | ID / ID |
| `name` | string | Название / Name |
| `phones` | string | Телефоны / Phones |

## Native endpoint

Through the native U-ON API, this operation is `GET /company-office.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-offices.md) for the provider-specific parameters and requirements.

