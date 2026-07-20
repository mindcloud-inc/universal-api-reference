# MoneyBird: List Administrations

Retrieves administrations from MoneyBird.

```
GET https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-administrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-administrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-administrations?${params}`, {
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
      "access": "string",
      "country": "string",
      "currency": "string",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "period_locked_until": "string",
      "period_start_date": "2026-05-07T12:00:00.000Z",
      "suspended": true,
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `period_locked_until` | string |  |
| `period_start_date` | date |  |
| `suspended` | boolean |  |
| `time_zone` | string |  |

## Native endpoint

Through the native MoneyBird API, this operation is `GET /administrations.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-administrations.md) for the provider-specific parameters and requirements.

