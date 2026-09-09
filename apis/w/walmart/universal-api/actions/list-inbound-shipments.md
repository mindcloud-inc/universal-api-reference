# Walmart: List Inbound Shipments

Retrieve a list of inbound shipments with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-inbound-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-inbound-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-inbound-shipments?${params}`, {
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
| `inboundOrderId` | string | no | Unique ID identifying inbound shipment request. |
| `shipmentId` | string | no | Unique ID identifying each shipment. |
| `status` | list<string> | no | Current shipment status. |
| `fromCreateDate` | date | no | Shipment create date starting range. Example: `2020-11-21T00:00:00.000Z` |
| `fromCreateDate_copy` | date | no | Shipment create date end range. Example: `2020-11-22T00:00:00.000Z` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrierName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "expectedDeliveryDate": "2026-05-07T12:00:00.000Z",
      "inboundOrderId": "string",
      "receivedUnits": 1,
      "returnAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "postalCode": "string",
        "stateCode": "string"
      },
      "shipmentId": "string",
      "shipmentUnits": 1,
      "shipToAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "fcName": "Ava Chen",
        "postalCode": "string",
        "stateCode": "string"
      },
      "status": "string",
      "trackingNo": [
        "string"
      ],
      "updatedExpectedDeliveryDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierName` | string |  |
| `createdDate` | date |  |
| `expectedDeliveryDate` | date |  |
| `inboundOrderId` | string |  |
| `receivedUnits` | number |  |
| `returnAddress.addressLine1` | string |  |
| `returnAddress.city` | string |  |
| `returnAddress.countryCode` | string |  |
| `returnAddress.postalCode` | string |  |
| `returnAddress.stateCode` | string |  |
| `shipmentId` | string |  |
| `shipmentUnits` | number |  |
| `shipToAddress.addressLine1` | string |  |
| `shipToAddress.city` | string |  |
| `shipToAddress.countryCode` | string |  |
| `shipToAddress.fcName` | string |  |
| `shipToAddress.postalCode` | string |  |
| `shipToAddress.stateCode` | string |  |
| `status` | string |  |
| `trackingNo[]` | string |  |
| `updatedExpectedDeliveryDate` | date |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/fulfillment/inbound-shipments` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inbound-shipments.md) for the provider-specific parameters and requirements.

