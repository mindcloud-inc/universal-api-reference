# Infoplus: Create External Shipment

Creates a new external shipment in Infoplus.

```
POST https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-external-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-external-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/create-external-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "modifyDate": "2026-05-07T12:00:00.000Z",
      "orderId": 1,
      "shipDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "trackingNo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | date |  |
| `id` | number |  |
| `modifyDate` | date |  |
| `orderId` | number |  |
| `shipDate` | date |  |
| `status` | string |  |
| `trackingNo` | string |  |

## Native endpoint

Through the native Infoplus API, this operation is `POST /externalShipment` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-external-shipment.md) for the provider-specific parameters and requirements.

