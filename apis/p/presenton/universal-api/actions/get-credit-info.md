# Presenton: Get Credit Info



```
GET https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-credit-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-credit-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-credit-info?${params}`, {
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
      "autoTopup": {
        "amount": 1,
        "enabled": true,
        "threshold": 1
      },
      "hasPaymentMethod": true,
      "rates": {
        "above100Cost": 1,
        "below100Cost": 1,
        "below25Cost": 1,
        "below50Cost": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoTopup.amount` | number |  |
| `autoTopup.enabled` | boolean |  |
| `autoTopup.threshold` | number |  |
| `hasPaymentMethod` | boolean |  |
| `rates.above100Cost` | number |  |
| `rates.below100Cost` | number |  |
| `rates.below25Cost` | number |  |
| `rates.below50Cost` | number |  |

## Native endpoint

Through the native Presenton API, this operation is `GET /api/v1/credit/info` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-info.md) for the provider-specific parameters and requirements.

