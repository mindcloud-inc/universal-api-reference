# ShipWise: Track Shipment

Retrieves shipment tracking details from ShipWise.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/track-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/track-shipment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/track-shipment?${params}`, {
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
| `trackingNumber` | string | no | Carrier tracking number to look up. Provide this or Package ID. Example: `1Z999AA10123456784`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | string | no | ShipWise package ID to look up. Provide this or Tracking Number. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "description": "string",
      "estimatedDeliveryDate": "2026-05-07T12:00:00.000Z",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
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
| `accountID` | string | ShipWise account number used to create the shipment. |
| `description` | string | Carrier delivery status description. |
| `estimatedDeliveryDate` | date | Estimated delivery date. |
| `lastUpdate` | date | Last carrier tracking update timestamp. |
| `shipDate` | date | Date the package shipped in ShipWise. |
| `statusName` | string | Delivery status name, such as Delivered or InTransit. |
| `trackingNumber` | string | Carrier tracking number. |

## Native endpoint

Through the native ShipWise API, this operation is `GET /api/v1/Ship/Tracking` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-shipment.md) for the provider-specific parameters and requirements.

