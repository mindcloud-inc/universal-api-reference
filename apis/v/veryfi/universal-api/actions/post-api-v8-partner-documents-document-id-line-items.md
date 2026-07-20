# Veryfi: Create a Line Item

Creates a line item in a document in Veryfi.

```
POST https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-documents-document-id-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-documents-document-id-line-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "value": "string",
  "boundingRegion[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/post-api-v8-partner-documents-document-id-line-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "value": "string",
    "boundingRegion[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `value` | string | yes | The category is taken from the line item with the same SKU and/or description. Otherwise from the root category field. string Possible values: >= 4 characters The value to update |
| `boundingRegion[]` | array<number> | yes | The date found on the document and associated with the line item in ISO 8601 format . string Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `order` | number | no |  |
| `expandedDescription` | string | no | Line item extra product info Possible values: non-empty Possible values: non-empty Possible values: non-empty |
| `tags[]` | array<string> | no | Possible values: non-empty A user-defined list of identifiers that help to categorize or flag particular types of line items. |

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

Through the native Veryfi API, this operation is `POST /api/v8/partner/documents/:document_id/line-items` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-api-v8-partner-documents-document-id-line-items.md) for the provider-specific parameters and requirements.

