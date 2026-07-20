# Tiliter: Get Product Sample

Retrieves a product sample from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-product-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-product-sample?connectionId=$CONNECTION_ID&productId=string&sampleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string",
  "sampleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/get-product-sample?${params}`, {
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
| `productId` | string | yes |  |
| `sampleId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerCode": "string",
      "id": "string",
      "productId": "string",
      "request": {
        "backgroundType": "string",
        "cameraType": "string",
        "collectorEmail": "ava@example.com",
        "deviceId": "string",
        "images": [
          {
            "cameraType": "string",
            "captureTime": "2026-05-07T12:00:00.000Z",
            "image": "string"
          }
        ],
        "product": {
          "archetypeId": "string",
          "archetypeName": "Ava Chen",
          "department": "string",
          "optionalAttributes": [
            "string"
          ],
          "productId": "string",
          "productName": "Ava Chen",
          "recognitionEnabled": true,
          "requiredAttributes": [
            "string"
          ]
        },
        "sampleType": "string",
        "weightGrams": 1
      },
      "requestMetadata": {
        "customerCode": "string",
        "requesterIp": "string",
        "requestReceiptTimestamp": "2026-05-07T12:00:00.000Z"
      },
      "sampleType": "string",
      "snapshotType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerCode` | string |  |
| `id` | string |  |
| `productId` | string |  |
| `request` | object |  |
| `request.backgroundType` | string |  |
| `request.cameraType` | string |  |
| `request.collectorEmail` | string |  |
| `request.deviceId` | string |  |
| `request.images` | array<object> |  |
| `request.images[].cameraType` | string |  |
| `request.images[].captureTime` | date |  |
| `request.images[].image` | string |  |
| `request.product` | object |  |
| `request.product.archetypeId` | string |  |
| `request.product.archetypeName` | string |  |
| `request.product.department` | string |  |
| `request.product.optionalAttributes` | array |  |
| `request.product.productId` | string |  |
| `request.product.productName` | string |  |
| `request.product.recognitionEnabled` | boolean |  |
| `request.product.requiredAttributes` | array |  |
| `request.sampleType` | string |  |
| `request.weightGrams` | number |  |
| `requestMetadata` | object |  |
| `requestMetadata.customerCode` | string |  |
| `requestMetadata.requesterIp` | string |  |
| `requestMetadata.requestReceiptTimestamp` | date |  |
| `sampleType` | string |  |
| `snapshotType` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /products/:product_id/samples/:sample_id` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-sample.md) for the provider-specific parameters and requirements.

