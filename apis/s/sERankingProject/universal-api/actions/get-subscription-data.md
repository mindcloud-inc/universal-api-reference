# SE Ranking Project: Get Subscription Data

Retrieves SE Ranking subscription details and account balance.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-subscription-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-subscription-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-subscription-data?${params}`, {
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
      "balance": {
        "amount": "string",
        "currency": "string"
      },
      "isExpired": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | object |  |
| `balance.amount` | string |  |
| `balance.currency` | string |  |
| `isExpired` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /account/subscription` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription-data.md) for the provider-specific parameters and requirements.

