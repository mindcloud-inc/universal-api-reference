# Amazon Seller: List Shipment Items

Retrieves inbound shipment items from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-items?connectionId=$CONNECTION_ID&marketplaceID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "marketplaceID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-shipment-items?${params}`, {
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
| `marketplaceID` | list<string> | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `lastUpdatedAfter` | string | no | A date used for selecting inbound shipment items that were last updated after (or at) a specified time. The selection includes updates made by Amazon and by the seller. |
| `lastUpdatedBefore` | string | no | A date used for selecting inbound shipment items that were last updated before (or at) a specified time. The selection includes updates made by Amazon and by the seller. |

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

Through the native Amazon Seller API, this operation is `GET fba/inbound/v0/shipmentItems` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-items.md) for the provider-specific parameters and requirements.

