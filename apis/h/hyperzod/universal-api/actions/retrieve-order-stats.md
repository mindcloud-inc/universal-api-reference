# Hyperzod: Retrieve Order Stats

Retrieves order statistics from Hyperzod by delivery date.

```
GET https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/retrieve-order-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperzod `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/retrieve-order-stats?connectionId=$CONNECTION_ID&deliveryTimestampFrom=string&deliveryTimestampTo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deliveryTimestampFrom": "string",
  "deliveryTimestampTo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/retrieve-order-stats?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryTimestampFrom` | string | yes |  |
| `deliveryTimestampTo` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the Hyperzod request completed successfully. |

## Native endpoint

Through the native Hyperzod API, this operation is `GET /admin/v1/order/stats` (base URL `https://api.hyperzod.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-stats.md) for the provider-specific parameters and requirements.

