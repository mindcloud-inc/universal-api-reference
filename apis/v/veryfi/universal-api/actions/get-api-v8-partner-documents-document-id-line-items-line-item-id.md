# Veryfi: Get a Line Item

Retrieves a line item from a document in Veryfi.

```
GET https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-line-items-line-item-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-line-items-line-item-id?connectionId=$CONNECTION_ID&documentId=string&lineItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "lineItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/get-api-v8-partner-documents-document-id-line-items-line-item-id?${params}`, {
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
| `documentId` | string | yes |  |
| `lineItemId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "country_of_origin": "string",
      "custom_fields": "string",
      "date": "string",
      "description": "string",
      "discount": 1,
      "discount_price": 1,
      "discount_rate": 1,
      "end_date": "string",
      "expanded_description": "string",
      "full_description": "string",
      "gross_total": 1,
      "hsn": "string",
      "id": 1,
      "lot": "string",
      "manufacturer": "string",
      "net_total": 1,
      "normalized_description": "string",
      "order": 1,
      "price": 1,
      "product_details": [
        {}
      ],
      "quantity": 1,
      "reference": "string",
      "section": "string",
      "sku": "string",
      "start_date": "string",
      "subtotal": 1,
      "tags": [
        "string"
      ],
      "tax": 1,
      "tax_code": "string",
      "tax_rate": 1,
      "text": "string",
      "total": 1,
      "type": "string",
      "unit_of_measure": "string",
      "upc": "string",
      "weight": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `country_of_origin` | string |  |
| `custom_fields` | string |  |
| `date` | string |  |
| `description` | string |  |
| `discount` | number |  |
| `discount_price` | number |  |
| `discount_rate` | number |  |
| `end_date` | string |  |
| `expanded_description` | string |  |
| `full_description` | string |  |
| `gross_total` | number |  |
| `hsn` | string |  |
| `id` | number |  |
| `lot` | string |  |
| `manufacturer` | string |  |
| `net_total` | number |  |
| `normalized_description` | string |  |
| `order` | number |  |
| `price` | number |  |
| `product_details` | array<object> |  |
| `quantity` | number |  |
| `reference` | string |  |
| `section` | string |  |
| `sku` | string |  |
| `start_date` | string |  |
| `subtotal` | number |  |
| `tags` | array<string> |  |
| `tax` | number |  |
| `tax_code` | string |  |
| `tax_rate` | number |  |
| `text` | string |  |
| `total` | number |  |
| `type` | string |  |
| `unit_of_measure` | string |  |
| `upc` | string |  |
| `weight` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `GET /api/v8/partner/documents/:document_id/line-items/:line_item_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-v8-partner-documents-document-id-line-items-line-item-id.md) for the provider-specific parameters and requirements.

