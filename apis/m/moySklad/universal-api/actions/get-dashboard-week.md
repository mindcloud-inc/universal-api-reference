# MoySklad: Get dashboard week

Retrieves the dashboard week from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-dashboard-week
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-dashboard-week?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-dashboard-week?${params}`, {
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
      "money": 1,
      "orders": 1,
      "profit": 1,
      "sales": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `money` | number |  |
| `orders` | number |  |
| `profit` | number |  |
| `sales` | number |  |
| `updated` | date |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET report/dashboard/week` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-week.md) for the provider-specific parameters and requirements.

