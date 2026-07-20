# RO App: Get Company



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-company?${params}`, {
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
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "currency_symbol": "string",
      "email": "ava@example.com",
      "logo": "string",
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `currency_symbol` | string |  |
| `email` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /company` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

