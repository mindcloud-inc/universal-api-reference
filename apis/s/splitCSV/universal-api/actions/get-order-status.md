# Split CSV: Get Order Status

Retrieves the status of an order in Split CSV.

```
GET https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/get-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Split CSV `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/get-order-status?connectionId=$CONNECTION_ID&id=latest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "latest"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/get-order-status?${params}`, {
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
| `id` | string | yes | The order ID returned by Create Order. Use latest to retrieve the most recent order. Example: `latest`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | A download URL for the completed split archive when available. |
| `created` | date | The order creation timestamp in ISO8601 format. |
| `id` | string | The order id. |
| `name` | string | The order name, typically driven by the source file name. |
| `status` | string | The current order status. |
| `updated` | date | The most recent order update timestamp in ISO8601 format. |

## Native endpoint

Through the native Split CSV API, this operation is `GET /app/api/v1/orders/:id/status` (base URL `https://www.splitcsv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-status.md) for the provider-specific parameters and requirements.

