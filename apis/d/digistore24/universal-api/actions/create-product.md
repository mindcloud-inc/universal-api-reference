# Digistore24: Create Product

Creates a new product in Digistore24.

```
POST https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Product properties object |
| `data.nameIntern` | string | no | Internal product name |
| `data.nameDe` | string | no | German product name |
| `data.nameEn` | string | no | English product name |
| `data.nameEs` | string | no | Spanish product name |
| `data.descriptionDe` | string | no | German product description |
| `data.descriptionEn` | string | no | English product description |
| `data.descriptionEs` | string | no | Spanish product description |
| `data.salespageUrl` | string | no | Sales page URL |
| `data.upsellSalespageUrl` | string | no | Upsell sales page URL |
| `data.thankyouUrl` | string | no | Thank you page URL |
| `data.imageUrl` | string | no | Product image URL |
| `data.productTypeId` | number | no | Product type ID |
| `data.approvalStatus` | string | no | Product approval status |
| `data.affiliateCommission` | number | no | Affiliate commission amount |
| `data.buyerType` | string | no | Buyer type |
| `data.isAddressInputMandatory` | string | no | Whether address input is mandatory |
| `data.addOrderDataToThankyouPageUrl` | string | no | Whether to append order data to the thank you URL |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `POST /createProduct` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

