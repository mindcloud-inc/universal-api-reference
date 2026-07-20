# Remote Retrieval: Get Device Prices

Retrieves device prices from Remote Retrieval.

```
GET https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/get-device-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Remote Retrieval `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/get-device-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remoteRetrieval/latest/actions/get-device-prices?${params}`, {
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
      "equipment_type": "string",
      "option_lbl": 1,
      "order_amount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `equipment_type` | string | Device or equipment category. |
| `option_lbl` | number | Runtime option label value returned by Remote Retrieval for the device category. |
| `order_amount` | number | Current order amount for the device category. |

## Native endpoint

Through the native Remote Retrieval API, this operation is `GET /api/v1/get-device-prices` (base URL `https://www.remoteretrieval.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-prices.md) for the provider-specific parameters and requirements.

