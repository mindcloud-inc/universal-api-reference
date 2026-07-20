# ShipWise: Query Shipments

Finds shipments in ShipWise by query.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/query-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/query-shipments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/query-shipments?${params}`, {
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
| `department` | string | no | Optional department criterion for shipment queries. Example: `Retail`. |
| `shippingProfileId` | string | no | Optional shipping profile ID criterion for shipment queries. Example: `123`. |
| `marketIds` | string | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "department": "string",
      "id": "string",
      "shipDate": "2026-05-07T12:00:00.000Z",
      "shippingProfileId": "string",
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
| `department` | string | Department query/result field when returned. |
| `id` | string | Shipment identifier. |
| `shipDate` | date | Shipment date. |
| `shippingProfileId` | string | Shipping profile identifier when returned. |
| `statusName` | string | Shipment status. |
| `trackingNumber` | string | Carrier tracking number. |

## Native endpoint

Through the native ShipWise API, this operation is `POST /api/v1/Ship/Query` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-shipments.md) for the provider-specific parameters and requirements.

