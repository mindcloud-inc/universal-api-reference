# LimoExpress: Update Payment Method

Updates an existing payment method in LimoExpress.

```
PUT https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/update-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/update-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/update-payment-method', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Operation payload when returned by the API. |
| `message` | string | Operation status or error message. |
| `success` | boolean | Operation success flag when provided by the API. |

## Native endpoint

Through the native LimoExpress API, this operation is `POST /api/integration/payment-methods` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-method.md) for the provider-specific parameters and requirements.

