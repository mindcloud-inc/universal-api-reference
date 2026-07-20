# ShipWise: Get Shipment

Retrieves a shipment from ShipWise.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/get-shipment?connectionId=$CONNECTION_ID&id=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/get-shipment?${params}`, {
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
| `id` | string | yes | ShipWise shipment ID. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "packingElapsedTime": "string",
      "shipDate": "2026-05-07T12:00:00.000Z",
      "statusName": "Ava Chen",
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Shipment identifier. |
| `packingElapsedTime` | string | Packing elapsed time field documented for GET /api/v1/Ship/{id} responses. |
| `shipDate` | date | Shipment date. |
| `statusName` | string | Shipment status. |
| `trackingNumber` | string | Carrier tracking number. |

## Native endpoint

Through the native ShipWise API, this operation is `GET /api/v1/Ship/:id` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

