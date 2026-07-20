# EasyPost: List Shipments

Retrieves a list of shipments from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-shipments?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "mode": "string",
      "object": "string",
      "postageLabel": {},
      "rates": [
        {}
      ],
      "selectedRate": {},
      "status": "string",
      "tracker": {},
      "trackingCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | EasyPost Shipment ID. |
| `mode` | string | EasyPost mode. |
| `object` | string | EasyPost object type. |
| `postageLabel` | object | Shipment postage label. |
| `rates` | array<object> | Available shipment rates. |
| `selectedRate` | object | Purchased or selected rate. |
| `status` | string | Shipment status. |
| `tracker` | object | Associated tracker. |
| `trackingCode` | string | Shipment tracking code. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native EasyPost API, this operation is `GET /shipments` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

