# Cloudprinter.com: List Orders

Retrieves orders from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-orders?${params}`, {
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
      "order_date": "string",
      "reference": "string",
      "state": 1,
      "state_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order_date` | string |  |
| `reference` | string |  |
| `state` | number |  |
| `state_code` | string |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/orders/` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

