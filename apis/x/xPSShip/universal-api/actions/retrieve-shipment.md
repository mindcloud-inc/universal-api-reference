# XPS Ship: Retrieve Shipment

Retrieves a shipment from XPS Ship.

```
GET https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/retrieve-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/retrieve-shipment?connectionId=$CONNECTION_ID&bookNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/retrieve-shipment?${params}`, {
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
| `bookNumber` | string | yes | XPS Ship shipment book number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookNumber": "string",
      "carrierCode": "string",
      "packageTypeCode": "string",
      "pieces": [
        {}
      ],
      "receiver": {},
      "sender": {},
      "serviceCode": "string",
      "shipmentDate": "string",
      "totalShippingCost": 1,
      "trackingNumber": "string",
      "trackingNumbers": [
        "string"
      ],
      "voided": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookNumber` | string |  |
| `carrierCode` | string |  |
| `packageTypeCode` | string |  |
| `pieces` | array<object> |  |
| `receiver` | object |  |
| `sender` | object |  |
| `serviceCode` | string |  |
| `shipmentDate` | string |  |
| `totalShippingCost` | number |  |
| `trackingNumber` | string |  |
| `trackingNumbers` | array<string> |  |
| `voided` | boolean |  |

## Native endpoint

Through the native XPS Ship API, this operation is `GET /restapi/v1/customers/:customerId/shipments/:bookNumber` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-shipment.md) for the provider-specific parameters and requirements.

