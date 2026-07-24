# Cin7 Core: List Carriers



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-carriers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-carriers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/list-carriers?${params}`, {
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
| `CarrierID` | string | no |  |
| `Description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fulfillmentNumber": 1,
      "fulFilmentStatus": "string",
      "linkedInvoiceNumber": {},
      "pack": {
        "lines": [
          {
            "batchSN": {},
            "box": "string",
            "expiryDate": {},
            "location": "string",
            "locationID": "string",
            "name": "Ava Chen",
            "nonInventory": true,
            "productID": "string",
            "quantity": 1,
            "sku": "string",
            "warrantyRegistrationNumber": {}
          }
        ],
        "status": "string"
      },
      "pick": {
        "lines": [
          {
            "batchSN": {},
            "comment": {},
            "expiryDate": {},
            "location": "string",
            "locationID": "string",
            "name": "Ava Chen",
            "nonInventory": true,
            "productID": "string",
            "quantity": 1,
            "restockDate": {},
            "restockLocation": {},
            "restockLocationID": {},
            "sku": "string"
          }
        ],
        "status": "string"
      },
      "ship": {
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
        "status": "string"
      },
      "taskID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fulfillmentNumber` | number |  |
| `fulFilmentStatus` | string |  |
| `linkedInvoiceNumber` | object |  |
| `pack.lines[].batchSN` | object |  |
| `pack.lines[].box` | string |  |
| `pack.lines[].expiryDate` | object |  |
| `pack.lines[].location` | string |  |
| `pack.lines[].locationID` | string |  |
| `pack.lines[].name` | string |  |
| `pack.lines[].nonInventory` | boolean |  |
| `pack.lines[].productID` | string |  |
| `pack.lines[].quantity` | number |  |
| `pack.lines[].sku` | string |  |
| `pack.lines[].warrantyRegistrationNumber` | object |  |
| `pack.status` | string |  |
| `pick.lines[].batchSN` | object |  |
| `pick.lines[].comment` | object |  |
| `pick.lines[].expiryDate` | object |  |
| `pick.lines[].location` | string |  |
| `pick.lines[].locationID` | string |  |
| `pick.lines[].name` | string |  |
| `pick.lines[].nonInventory` | boolean |  |
| `pick.lines[].productID` | string |  |
| `pick.lines[].quantity` | number |  |
| `pick.lines[].restockDate` | object |  |
| `pick.lines[].restockLocation` | object |  |
| `pick.lines[].restockLocationID` | object |  |
| `pick.lines[].sku` | string |  |
| `pick.status` | string |  |
| `ship.lines[].boxes` | string |  |
| `ship.lines[].carrier` | string |  |
| `ship.lines[].id` | string |  |
| `ship.lines[].isShipped` | boolean |  |
| `ship.lines[].shipmentDate` | string |  |
| `ship.lines[].trackingNumber` | string |  |
| `ship.lines[].trackingURL` | string |  |
| `ship.requireBy` | string |  |
| `ship.shippingAddress.city` | string |  |
| `ship.shippingAddress.company` | string |  |
| `ship.shippingAddress.contact` | string |  |
| `ship.shippingAddress.country` | string |  |
| `ship.shippingAddress.displayAddressLine1` | string |  |
| `ship.shippingAddress.displayAddressLine2` | string |  |
| `ship.shippingAddress.line1` | string |  |
| `ship.shippingAddress.line2` | string |  |
| `ship.shippingAddress.postcode` | string |  |
| `ship.shippingAddress.shipToOther` | boolean |  |
| `ship.shippingAddress.state` | string |  |
| `ship.shippingNotes` | string |  |
| `ship.status` | string |  |
| `taskID` | string |  |

## Native endpoint

Through the native Cin7 Core API, this operation is `GET ref/carrier` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-carriers.md) for the provider-specific parameters and requirements.

