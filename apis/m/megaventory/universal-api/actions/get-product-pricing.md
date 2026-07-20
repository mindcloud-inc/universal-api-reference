# Megaventory: Get Product Pricing

Retrieves pricing for a product from Megaventory.

```
GET https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/get-product-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/get-product-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/get-product-pricing?${params}`, {
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
| `ProductId` | number | no | Megaventory product ID to price. |
| `DocumentTypeId` | number | no | Document type that affects the calculated price. |
| `Quantity` | number | no | Quantity used for the price lookup. |
| `SupplierClientId` | number | no | Supplier or client context for the price lookup. |
| `Currency` | string | no | Currency code for the requested price. |
| `IssueDate` | date | no | Date Megaventory should use when resolving the price. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "PricingDetails": [
        {}
      ],
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `PricingDetails` | array<object> |  |
| `ResponseStatus` | object |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/ProductPriceGet` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-pricing.md) for the provider-specific parameters and requirements.

