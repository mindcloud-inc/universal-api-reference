# Flexport: Retrieve Shipment

Retrieves a shipment from your Flexport account.

```
GET https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-shipment?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-shipment?${params}`, {
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
| `id` | number | yes | Unique Flexport shipment ID to retrieve. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airShipment": {},
      "calculatedVolume": {},
      "calculatedWeight": {},
      "cargoReadyDate": "2026-05-07T12:00:00.000Z",
      "consignees": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dangerousGoods": {},
      "documents": {},
      "freightCost": "string",
      "freightType": "string",
      "id": 1,
      "incoterm": "string",
      "items": [
        {}
      ],
      "legs": {},
      "name": "Ava Chen",
      "oceanShipment": {},
      "pieces": 1,
      "shippers": [
        {}
      ],
      "status": "string",
      "transportationMode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airShipment` | object |  |
| `calculatedVolume` | object |  |
| `calculatedWeight` | object |  |
| `cargoReadyDate` | date |  |
| `consignees` | array<object> |  |
| `createdAt` | date |  |
| `dangerousGoods` | object |  |
| `documents` | object |  |
| `freightCost` | string |  |
| `freightType` | string |  |
| `id` | number |  |
| `incoterm` | string |  |
| `items` | array<object> |  |
| `legs` | object |  |
| `name` | string |  |
| `oceanShipment` | object |  |
| `pieces` | number |  |
| `shippers` | array<object> |  |
| `status` | string |  |
| `transportationMode` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Flexport API, this operation is `GET /shipments/:id` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shipment.md) for the provider-specific parameters and requirements.

