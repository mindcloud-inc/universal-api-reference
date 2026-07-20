# BunnyCDN: Get Pending Payment Requests

Retrieves pending payment requests from BunnyCDN.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-pending-payment-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-pending-payment-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/get-pending-payment-requests?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of pending payment requests returned by Bunny. Empty when there are no pending requests. |

## Native endpoint

Through the native BunnyCDN API, this operation is `GET /billing/payment-requests` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pending-payment-requests.md) for the provider-specific parameters and requirements.

