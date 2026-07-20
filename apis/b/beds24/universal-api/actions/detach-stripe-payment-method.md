# Beds24: Detach Stripe Payment Method

Detaches a Stripe payment method from Beds24.

```
DELETE https://connect.mindcloud.co/v1/universal/beds24/latest/actions/detach-stripe-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/detach-stripe-payment-method?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/detach-stripe-payment-method?${params}`, {
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
      "errors": [
        {}
      ],
      "info": [
        {}
      ],
      "modified": {},
      "new": {},
      "success": true,
      "warnings": [
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
| `errors` | array<object> |  |
| `info` | array<object> |  |
| `modified` | object |  |
| `new` | object |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Beds24 API, this operation is `POST /channels/stripe` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-stripe-payment-method.md) for the provider-specific parameters and requirements.

