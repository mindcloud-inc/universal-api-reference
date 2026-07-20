# DMSales: Get Wallet Points

Retrieves wallet points from DMSales.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-wallet-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-wallet-points?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-wallet-points?${params}`, {
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
      "is_active_subscription": true,
      "is_completed_data": true,
      "is_it_mine": true,
      "is_phone_verified": true,
      "points": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_active_subscription` | boolean |  |
| `is_completed_data` | boolean |  |
| `is_it_mine` | boolean |  |
| `is_phone_verified` | boolean |  |
| `points` | object |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/user/wallet/points` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-points.md) for the provider-specific parameters and requirements.

