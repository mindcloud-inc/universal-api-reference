# Open Letter Connect: Get Product Details

Retrieves product details from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-details?connectionId=$CONNECTION_ID&productType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-details?${params}`, {
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
| `productType` | string | yes | The product type to inspect, for example Personal Letters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryDuration": {
        "First Class": "string",
        "First Class Forever": "string",
        "Standard Class": "string"
      },
      "deliveryType": [
        [
          "string"
        ]
      ],
      "envelopeType": [
        [
          "string"
        ]
      ],
      "paperSize": [
        [
          "string"
        ]
      ],
      "paperType": [
        [
          "string"
        ]
      ],
      "postageType": [
        [
          "string"
        ]
      ],
      "productType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryDuration.First Class` | string | Quoted delivery window for First Class delivery. |
| `deliveryDuration.First Class Forever` | string | Quoted delivery window for First Class Forever delivery. |
| `deliveryDuration.Standard Class` | string | Quoted delivery window for Standard Class delivery. |
| `deliveryType[]` | array<string> | Available delivery types for the selected product type. |
| `envelopeType[]` | array<string> | Available envelope types for the selected product type. |
| `paperSize[]` | array<string> | Available paper sizes for the selected product type. |
| `paperType[]` | array<string> | Available paper types for the selected product type. |
| `postageType[]` | array<string> | Available postage types for the selected product type. |
| `productType` | string | Product type that was queried. |

## Native endpoint

Through the native Open Letter Connect API, this operation is `POST /products/details` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-details.md) for the provider-specific parameters and requirements.

