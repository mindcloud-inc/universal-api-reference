# Cin7 Core: Get Sale Fulfillment Ship



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-fulfillment-ship
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-fulfillment-ship?connectionId=$CONNECTION_ID&TaskID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "TaskID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-fulfillment-ship?${params}`, {
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
| `TaskID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lines": [
        {
          "boxes": "string",
          "carrier": "string",
          "id": "string",
          "isShipped": true,
          "shipmentDate": "string",
          "trackingNumber": "string",
          "trackingURL": "https://example.com"
        }
      ],
      "requireBy": "string",
      "shippingAddress": {
        "city": "string",
        "company": "string",
        "contact": "string",
        "country": "string",
        "displayAddressLine1": "string",
        "displayAddressLine2": "string",
        "line1": "string",
        "line2": "string",
        "postcode": "string",
        "shipToOther": true,
        "state": "string"
      },
      "shippingNotes": "string",
      "status": "string",
      "taskID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lines[].boxes` | string |  |
| `lines[].carrier` | string |  |
| `lines[].id` | string |  |
| `lines[].isShipped` | boolean |  |
| `lines[].shipmentDate` | string |  |
| `lines[].trackingNumber` | string |  |
| `lines[].trackingURL` | string |  |
| `requireBy` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.company` | string |  |
| `shippingAddress.contact` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.displayAddressLine1` | string |  |
| `shippingAddress.displayAddressLine2` | string |  |
| `shippingAddress.line1` | string |  |
| `shippingAddress.line2` | string |  |
| `shippingAddress.postcode` | string |  |
| `shippingAddress.shipToOther` | boolean |  |
| `shippingAddress.state` | string |  |
| `shippingNotes` | string |  |
| `status` | string |  |
| `taskID` | string |  |

## Native endpoint

Through the native Cin7 Core API, this operation is `GET sale/fulfilment/ship` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale-fulfillment-ship.md) for the provider-specific parameters and requirements.

