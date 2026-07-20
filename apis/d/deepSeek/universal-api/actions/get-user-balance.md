# DeepSeek: Get User Balance



```
GET https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/get-user-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepSeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/get-user-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/get-user-balance?${params}`, {
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
      "balanceInfos": [
        {
          "currency": "string",
          "grantedBalance": "string",
          "toppedUpBalance": "string",
          "totalBalance": "string"
        }
      ],
      "isAvailable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceInfos[].currency` | string |  |
| `balanceInfos[].grantedBalance` | string |  |
| `balanceInfos[].toppedUpBalance` | string |  |
| `balanceInfos[].totalBalance` | string |  |
| `isAvailable` | boolean |  |

## Native endpoint

Through the native DeepSeek API, this operation is `GET /user/balance` (base URL `https://api.deepseek.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-balance.md) for the provider-specific parameters and requirements.

