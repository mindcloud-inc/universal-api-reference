# DateX: List Sales Shipments



```
GET https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-sales-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-sales-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-sales-shipments?${params}`, {
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
| `filters.orderLookup` | string | no | Sales order lookup filter. |
| `filters.lookup` | string | no | Shipment lookup filter. |
| `filters.carrier` | string | no | Carrier filter. |
| `excludeTransmitted` | boolean | no | Exclude transmitted shipments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrierService": "string",
      "createdOn": "string",
      "lookup": "string",
      "orderLookup": "string",
      "owner": "string",
      "project": "string",
      "shipmentId": 1,
      "shippedContents": [
        {}
      ],
      "shippedOn": "string",
      "shippingContainers": [
        {}
      ],
      "status": "string",
      "trackingIdentifier": "string",
      "warehouse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrierService` | string |  |
| `createdOn` | string |  |
| `lookup` | string |  |
| `orderLookup` | string |  |
| `owner` | string |  |
| `project` | string |  |
| `shipmentId` | number |  |
| `shippedContents` | array<object> |  |
| `shippedOn` | string |  |
| `shippingContainers` | array<object> |  |
| `status` | string |  |
| `trackingIdentifier` | string |  |
| `warehouse` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST sales_orders/shipments/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-shipments.md) for the provider-specific parameters and requirements.

