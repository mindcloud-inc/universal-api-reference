# OrderOut: Get Quotes

Retrieves delivery quotes from OrderOut.

```
GET https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/get-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OrderOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/get-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/get-quotes?${params}`, {
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
      "delivery_mins_from_now": 1,
      "id": 1,
      "pickup_mins_from_now": 1,
      "price": 1,
      "provider": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `delivery_mins_from_now` | number |  |
| `id` | number |  |
| `pickup_mins_from_now` | number |  |
| `price` | number |  |
| `provider` | string |  |
| `unit` | string |  |

## Native endpoint

Through the native OrderOut API, this operation is `POST /v2/delivery/quotes` (base URL `https://api.orderout.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quotes.md) for the provider-specific parameters and requirements.

