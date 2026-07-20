# PayTabs: Create Sadad Split Payout Payment Request



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-sadad-split-payout-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-sadad-split-payout-payment-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/create-sadad-split-payout-payment-request', {
  method: 'POST',
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
      "message": "string",
      "redirectUrl": "https://example.com",
      "tranRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartId` | string |  |
| `message` | string |  |
| `redirectUrl` | string |  |
| `tranRef` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/apm/sadad/ifs/request` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sadad-split-payout-payment-request.md) for the provider-specific parameters and requirements.

