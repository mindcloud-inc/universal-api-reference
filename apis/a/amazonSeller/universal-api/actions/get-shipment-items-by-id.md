# Amazon Seller: Get Shipment Items by ID

Retrieves items from an Amazon Seller inbound shipment.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-items-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-items-by-id?connectionId=$CONNECTION_ID&shipmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-items-by-id?${params}`, {
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
| `shipmentId` | string | yes | A shipment identifier used for selecting items in a specific inbound shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fulfillmentNetworkSKU": "string",
      "prepDetailsList": [
        {
          "prepInstruction": "string",
          "prepOwner": "string"
        }
      ],
      "quantityInCase": 1,
      "quantityReceived": 1,
      "quantityShipped": 1,
      "releaseDate": "string",
      "sellerSKU": "string",
      "shipmentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fulfillmentNetworkSKU` | string |  |
| `prepDetailsList[].prepInstruction` | string |  |
| `prepDetailsList[].prepOwner` | string |  |
| `quantityInCase` | number |  |
| `quantityReceived` | number |  |
| `quantityShipped` | number |  |
| `releaseDate` | string |  |
| `sellerSKU` | string |  |
| `shipmentId` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET fba/inbound/v0/shipments/:shipmentId/items` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-items-by-id.md) for the provider-specific parameters and requirements.

