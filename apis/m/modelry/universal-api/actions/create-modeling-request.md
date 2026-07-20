# Modelry: Create Modeling Request



```
POST https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-modeling-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modelry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-modeling-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelingRequest.title": "string",
  "modelingRequest.sku": "string",
  "modelingRequest.productId": 1,
  "modelingRequest.dimensions": "string",
  "modelingRequest.pipeline": "string",
  "modelingRequest.specificRequirements": "string",
  "modelingRequest.externalUrl": "https://example.com",
  "modeling_request.reference_file_blob_ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-modeling-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelingRequest.title": "string",
    "modelingRequest.sku": "string",
    "modelingRequest.productId": 1,
    "modelingRequest.dimensions": "string",
    "modelingRequest.pipeline": "string",
    "modelingRequest.specificRequirements": "string",
    "modelingRequest.externalUrl": "https://example.com",
    "modeling_request.reference_file_blob_ids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelingRequest.title` | string | yes | Modeling request title. |
| `modelingRequest.sku` | string | yes | Modeling request SKU. |
| `modelingRequest.productId` | number | yes | Associated product ID. |
| `modelingRequest.dimensions` | string | yes | Dimensions string. |
| `modelingRequest.pipeline` | string | yes | Pipeline, such as high_poly or low_poly. |
| `modelingRequest.specificRequirements` | string | yes | Specific modeling requirements. |
| `modelingRequest.externalUrl` | string | yes | External URL for the request. |
| `modeling_request.reference_file_blob_ids[]` | array<string> | yes | Signed blob IDs from uploads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "batchUid": {},
        "createdAt": "string",
        "customerQaUrl": {},
        "deliveredAt": {},
        "dimensions": "string",
        "inCustomerQa": true,
        "pipeline": "string",
        "previewImageUrl": "https://example.com",
        "price": {},
        "productId": 1,
        "productUrl": "https://example.com",
        "referenceFileUrls": [
          "https://example.com"
        ],
        "requestType": "string",
        "sku": "string",
        "status": "string",
        "title": "string",
        "uid": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.batchUid` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.customerQaUrl` | object |  |
| `attributes.deliveredAt` | object |  |
| `attributes.dimensions` | string |  |
| `attributes.inCustomerQa` | boolean |  |
| `attributes.pipeline` | string |  |
| `attributes.previewImageUrl` | string |  |
| `attributes.price` | object |  |
| `attributes.productId` | number |  |
| `attributes.productUrl` | string |  |
| `attributes.referenceFileUrls[]` | string |  |
| `attributes.requestType` | string |  |
| `attributes.sku` | string |  |
| `attributes.status` | string |  |
| `attributes.title` | string |  |
| `attributes.uid` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Modelry API, this operation is `POST /v1/modeling-requests` (base URL `https://api.modelry.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-modeling-request.md) for the provider-specific parameters and requirements.

