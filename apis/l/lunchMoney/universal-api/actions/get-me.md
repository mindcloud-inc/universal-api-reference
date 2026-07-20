# Lunch Money: Get current user



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-me?${params}`, {
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
      "accountId": 1,
      "apiKeyLabel": "string",
      "budgetName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "primaryCurrency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `apiKeyLabel` | string |  |
| `budgetName` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `primaryCurrency` | string |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /me` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-me.md) for the provider-specific parameters and requirements.

