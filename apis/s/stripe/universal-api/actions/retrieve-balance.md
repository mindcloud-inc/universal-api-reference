# Stripe: Retrieve Balance



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-balance?${params}`, {
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
      "available": [
        {}
      ],
      "connectReserved": [
        {}
      ],
      "livemode": true,
      "object": "string",
      "pending": [
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
| `available` | array<object> |  |
| `connectReserved` | array<object> |  |
| `livemode` | boolean |  |
| `object` | string |  |
| `pending` | array<object> |  |

## Native endpoint

Through the native Stripe API, this operation is `GET balance` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-balance.md) for the provider-specific parameters and requirements.

