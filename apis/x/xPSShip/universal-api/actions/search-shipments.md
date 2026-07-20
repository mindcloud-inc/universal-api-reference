# XPS Ship: Search Shipments

Finds booked shipments in XPS Ship by keyword.

```
GET https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/search-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/search-shipments?connectionId=$CONNECTION_ID&keyword=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/search-shipments?${params}`, {
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
| `keyword` | string | yes | Shipment search keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookNumber": "string",
      "carrierCode": "string",
      "orderIds": [
        "string"
      ],
      "packageTypeCode": "string",
      "serviceCode": "string",
      "shipmentDate": "string",
      "shipments": [
        {}
      ],
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
| `orderIds` | array<string> |  |
| `packageTypeCode` | string |  |
| `serviceCode` | string |  |
| `shipmentDate` | string |  |
| `shipments` | array<object> |  |
| `trackingNumber` | string |  |
| `trackingNumbers` | array<string> |  |
| `voided` | boolean |  |

## Native endpoint

Through the native XPS Ship API, this operation is `POST /restapi/v1/customers/:customerId/searchShipments` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-shipments.md) for the provider-specific parameters and requirements.

