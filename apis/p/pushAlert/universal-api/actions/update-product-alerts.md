# PushAlert: Update Product Alerts



```
PUT https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/update-product-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/update-product-alerts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productInfo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/update-product-alerts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productInfo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productInfo` | string | yes | JSON object string describing the product and changed field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Provider message returned for the product alert update request. |
| `success` | boolean | Whether the product alert update request succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `POST /rest/v2/web-push/product/update` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-alerts.md) for the provider-specific parameters and requirements.

