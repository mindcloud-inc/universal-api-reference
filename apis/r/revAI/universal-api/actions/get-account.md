# Rev AI: Get Account

Retrieves account details from Rev AI.

```
GET https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rev AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revAI/latest/actions/get-account?${params}`, {
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
      "balanceSeconds": 1,
      "email": "ava@example.com",
      "freeBalance": 1,
      "hipaaEnabled": true,
      "purchasedBalance": 1,
      "totalBalance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceSeconds` | number |  |
| `email` | string |  |
| `freeBalance` | number |  |
| `hipaaEnabled` | boolean |  |
| `purchasedBalance` | number |  |
| `totalBalance` | number |  |

## Native endpoint

Through the native Rev AI API, this operation is `GET /speechtotext/v1/account` (base URL `https://api.rev.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

