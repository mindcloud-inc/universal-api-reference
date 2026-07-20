# EasyPost: Get Shipment

Retrieves details for a shipment from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-shipment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-shipment?${params}`, {
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
| `id` | string | yes | EasyPost Shipment ID, beginning with shp_. |

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

Through the native EasyPost API, this operation is `GET /shipments/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

