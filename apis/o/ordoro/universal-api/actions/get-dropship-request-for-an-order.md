# Ordoro: Get Dropship Request for an Order

Retrieves a dropship request for an Ordoro order.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-dropship-request-for-an-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-dropship-request-for-an-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-dropship-request-for-an-order?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Ordoro API, this operation is `GET /v3/order/{order_number}/dropship` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dropship-request-for-an-order.md) for the provider-specific parameters and requirements.

