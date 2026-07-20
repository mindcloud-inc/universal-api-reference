# Amazon Seller: Get Labels

Retrieves inbound shipment labels from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-labels?connectionId=$CONNECTION_ID&limit=25&offset=0&shipmentId=string&pageType=string&labelType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shipmentId": "string",
  "pageType": "string",
  "labelType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-labels?${params}`, {
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
| `shipmentId` | string | yes | A shipment identifier originally returned by the `createInboundShipmentPlan` operation. |
| `pageType` | list<string> | yes | The page type to use to print the labels. Submitting a PageType value that is not supported in your marketplace returns an error. |
| `labelType` | list<string> | yes | The type of labels being requested. |
| `numberOfPackages` | number | no | The number of packages in the shipment. (optional) |
| `numberOfPallets` | number | no | The number of pallets in the shipment. This returns four identical labels for each pallet. |
| `packageLabelsToPrint` | string | no | A list of identifiers that specify packages for which you want package labels printed. Note: ``` If you provide box content information with the FBA Inbound Shipment Carton Information Feed, then PackageLabelsToPrint must match the CartonId values you provide through that feed. If you provide box content information with the Fulfillment Inbound API v2024-03-20, then PackageLabelsToPrint must match the boxID values from the listShipmentBoxes response. If these values do not match as required, the operation returns the IncorrectPackageIdentifier error code. ``` Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadURL` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET fba/inbound/v0/shipments/:shipmentId/label` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-labels.md) for the provider-specific parameters and requirements.

