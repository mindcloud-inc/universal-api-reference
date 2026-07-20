# Amazon Seller: List Shipments

Retrieves inbound shipments from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-inbound-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-inbound-shipments?connectionId=$CONNECTION_ID&queryType=string&marketplaceID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryType": "string",
  "marketplaceID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-inbound-shipments?${params}`, {
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
| `queryType` | list<string> | yes | Select how you want to look up shipments. You can search by specific IDs/Statuses or a Date Range. |
| `marketplaceID` | list<string> | yes | A marketplace identifier. Specifies the marketplace where the product would be stored. |
| `ShipmentStatusList` | list<string> | no | Return inbound shipments with a current status that matches the status values you specify. - WORKING The shipment was created by the seller, but has not yet shipped. - READY_TO_SHIP The seller has printed box labels (for Small parcel shipments) or pallet labels (for Less Than Truckload shipments). - SHIPPED The shipment was picked up by the carrier. - RECEIVING The shipment has arrived at the fulfillment center, but not all items have been marked as received. - CANCELLED The shipment was cancelled by the seller after the shipment was sent to the fulfillment center. - DELETED The shipment was cancelled by the seller before the shipment was sent to the fulfillment center. - CLOSED The shipment has arrived at the fulfillment center and all items have been marked as received. - ERROR There was an error with the shipment and it was not processed by Amazon. - IN_TRANSIT The carrier has notified the fulfillment center that it is aware of the shipment. - DELIVERED The shipment was delivered by the carrier to the fulfillment center. - CHECKED_IN The shipment was checked-in at the receiving dock of the fulfillment center. Accepts multiple values as an array. |
| `shipmentIdList` | string | no | A list of shipment IDs used to select the shipments that you want. If both `ShipmentStatusList` and `ShipmentIdList` are specified, only shipments that match both parameters are returned. Array of strings, max length: `999` Accepts multiple values as an array. |
| `lastUpdatedAfter` | string | no | A date used for selecting inbound shipments that were last updated after (or at) a specified time. The selection includes updates made by Amazon and by the seller. |
| `lastUpdatedBefore` | string | no | A date used for selecting inbound shipments that were last updated before (or at) a specified time. The selection includes updates made by Amazon and by the seller. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areCasesRequired": true,
      "boxContentsSource": "string",
      "destinationFulfillmentCenterId": "string",
      "labelPrepType": "string",
      "shipFromAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "name": "Ava Chen",
        "postalCode": "string",
        "stateOrProvinceCode": "string"
      },
      "shipmentId": "string",
      "shipmentName": "Ava Chen",
      "shipmentStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areCasesRequired` | boolean |  |
| `boxContentsSource` | string |  |
| `destinationFulfillmentCenterId` | string |  |
| `labelPrepType` | string |  |
| `shipFromAddress.addressLine1` | string |  |
| `shipFromAddress.city` | string |  |
| `shipFromAddress.countryCode` | string |  |
| `shipFromAddress.name` | string |  |
| `shipFromAddress.postalCode` | string |  |
| `shipFromAddress.stateOrProvinceCode` | string |  |
| `shipmentId` | string |  |
| `shipmentName` | string |  |
| `shipmentStatus` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET fba/inbound/v0/shipments` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inbound-shipments.md) for the provider-specific parameters and requirements.

