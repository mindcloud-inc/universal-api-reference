# TrackMage: Get Shipment Item

Retrieves a shipment item from TrackMage.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-shipment-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-shipment-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-shipment-item?${params}`, {
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
| `id` | string | yes | Resource identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalSourceIntegration": "string",
      "externalSourceSyncId": "string",
      "fulfillmentIntegration": "string",
      "fulfillmentSyncId": "string",
      "id": "string",
      "orderItem": "string",
      "qty": 1,
      "shipment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalSourceIntegration` | string |  |
| `externalSourceSyncId` | string |  |
| `fulfillmentIntegration` | string |  |
| `fulfillmentSyncId` | string |  |
| `id` | string |  |
| `orderItem` | string |  |
| `qty` | number |  |
| `shipment` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `GET /shipment_items/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-item.md) for the provider-specific parameters and requirements.

