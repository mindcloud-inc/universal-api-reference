# Digistore24: Update Product

Updates an existing product in Digistore24.

```
PUT https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | Product ID |
| `nameDe` | string | no | Product name in German |
| `nameEn` | string | no | Product name in English |
| `nameEs` | string | no | Product name in Spanish |
| `nameIntern` | string | no | Internal product name |
| `descriptionDe` | string | no | Product description in German |
| `descriptionEn` | string | no | Product description in English |
| `descriptionEs` | string | no | Product description in Spanish |
| `salespageUrl` | string | no | Sales page URL |
| `upsellSalespageUrl` | string | no | Upsell sales page URL |
| `thankyouUrl` | string | no | Thank you page URL |
| `imageUrl` | string | no | Product image URL |
| `productTypeId` | number | no | Product type ID |
| `currency` | string | no | Currencies for payments |
| `approvalStatus` | string | no | Approval status |
| `affiliateCommision` | number | no | Commission for affiliates |
| `buyerType` | string | no | Buyer type |
| `isAddressInputMandatory` | boolean | no | Whether buyer address input is mandatory |
| `addOrderDataToThankyouPageUrl` | boolean | no | Whether order data is added to the thank you URL |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `PUT /updateProduct` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

