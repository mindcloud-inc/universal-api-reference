# PayTabs: Extend Authorization



```
PUT https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/extend-authorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/extend-authorization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/extend-authorization', {
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
      "cartId": "string",
      "code": 1,
      "message": "string",
      "paymentResult": {},
      "trace": "string",
      "tranRef": "string",
      "tranType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartId` | string |  |
| `code` | number |  |
| `message` | string |  |
| `paymentResult` | object |  |
| `trace` | string |  |
| `tranRef` | string |  |
| `tranType` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/request` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-authorization.md) for the provider-specific parameters and requirements.

