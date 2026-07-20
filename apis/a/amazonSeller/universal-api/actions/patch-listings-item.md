# Amazon Seller: Patch Listings Item

Updates an existing listings item in Amazon Seller.

```
PUT https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/patch-listings-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/patch-listings-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sellerId": "string",
  "sku": "string",
  "marketplaceIds": "ATVPDKIKX0DER",
  "productType": "PRODUCT",
  "patches[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/patch-listings-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sellerId": "string",
    "sku": "string",
    "marketplaceIds": "ATVPDKIKX0DER",
    "productType": "PRODUCT",
    "patches[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sellerId` | string | yes |  |
| `sku` | string | yes |  |
| `marketplaceIds` | string<string> | yes | Default: `ATVPDKIKX0DER`. |
| `mode` | string | no | Set to `VALIDATION_PREVIEW` to validate the patch request without persisting listing changes. Example: `VALIDATION_PREVIEW`. |
| `productType` | string | yes | Default: `PRODUCT`. Example: `PRODUCT`. |
| `patches[]` | array | yes | Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issues": [
        [
          {}
        ]
      ],
      "sku": "string",
      "status": "string",
      "submissionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issues[]` | array<object> | Validation or processing issues returned by Amazon for the listing update. |
| `issues[].attributeNames[]` | array<string> | Attribute names related to the issue when Amazon provides them. |
| `issues[].categories[]` | array<string> | Issue categories returned by Amazon when available. |
| `issues[].code` | string | Amazon issue code. |
| `issues[].message` | string | Human-readable validation or processing message from Amazon. |
| `issues[].severity` | string | Issue severity returned by Amazon. |
| `sku` | string | Selling partner SKU submitted in the patch request. |
| `status` | string | Submission status returned by Amazon, such as ACCEPTED or INVALID. |
| `submissionId` | string | Amazon submission identifier for the listings patch request. |

## Native endpoint

Through the native Amazon Seller API, this operation is `PATCH listings/2021-08-01/items/:sellerId/:sku` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-listings-item.md) for the provider-specific parameters and requirements.

