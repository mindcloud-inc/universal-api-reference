# Shopkit: List Shipments

Retrieves shipments from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-shipments?${params}`, {
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
      "carrier": "string",
      "carrier_description": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "from": {},
      "order_id": "string",
      "to": {},
      "tracking_code": "string",
      "tracking_url": "https://example.com",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrier_description` | string |  |
| `created_at` | date |  |
| `from` | object |  |
| `order_id` | string |  |
| `to` | object |  |
| `tracking_code` | string |  |
| `tracking_url` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /shipment` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

