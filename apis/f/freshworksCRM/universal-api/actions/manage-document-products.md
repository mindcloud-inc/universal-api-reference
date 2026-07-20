# Freshworks CRM: Manage Document Products

Updates products on a document in Freshworks CRM.

```
PUT https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-document-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-document-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/manage-document-products', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `products[]` | array<object> | no |  |
| `products[].id` | number | no |  |
| `products[].quantity` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cpq_document": {
        "amount": 1,
        "base_currency_amount": 1,
        "contact_id": 1,
        "cpq_document_template_name": "Ava Chen",
        "cpq_signature_limit": 1,
        "cpq_signatures_used": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "creater_id": 1,
        "currency_code": "string",
        "deal_id": 1,
        "display_name": "Ava Chen",
        "document_number": "string",
        "document_type": "string",
        "has_products": true,
        "has_signatures": true,
        "id": 1,
        "is_deal_primary": true,
        "is_deleted": true,
        "owner_id": 1,
        "pricing_table_settings": "string",
        "products": [
          {
            "association_id": 1,
            "billing_type": 1,
            "cpq_document_id": 1,
            "currency_code": "string",
            "discount": 1,
            "discount_type": 1,
            "id": 1,
            "item_id": "string",
            "name": "Ava Chen",
            "owner_id": 1,
            "pricing_type": 1,
            "product_id": 1,
            "quantity": 1,
            "setup_fee": 1,
            "unit_price": 1
          }
        ],
        "sales_account_id": 1,
        "signing_order_modified": true,
        "stage": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "updater_id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cpq_document.amount` | number |  |
| `cpq_document.base_currency_amount` | number |  |
| `cpq_document.contact_id` | number |  |
| `cpq_document.cpq_document_template_name` | string |  |
| `cpq_document.cpq_signature_limit` | number |  |
| `cpq_document.cpq_signatures_used` | number |  |
| `cpq_document.created_at` | date |  |
| `cpq_document.creater_id` | number |  |
| `cpq_document.currency_code` | string |  |
| `cpq_document.deal_id` | number |  |
| `cpq_document.display_name` | string |  |
| `cpq_document.document_number` | string |  |
| `cpq_document.document_type` | string |  |
| `cpq_document.has_products` | boolean |  |
| `cpq_document.has_signatures` | boolean |  |
| `cpq_document.id` | number |  |
| `cpq_document.is_deal_primary` | boolean |  |
| `cpq_document.is_deleted` | boolean |  |
| `cpq_document.owner_id` | number |  |
| `cpq_document.pricing_table_settings` | string |  |
| `cpq_document.products[].association_id` | number |  |
| `cpq_document.products[].billing_type` | number |  |
| `cpq_document.products[].cpq_document_id` | number |  |
| `cpq_document.products[].currency_code` | string |  |
| `cpq_document.products[].discount` | number |  |
| `cpq_document.products[].discount_type` | number |  |
| `cpq_document.products[].id` | number |  |
| `cpq_document.products[].item_id` | string |  |
| `cpq_document.products[].name` | string |  |
| `cpq_document.products[].owner_id` | number |  |
| `cpq_document.products[].pricing_type` | number |  |
| `cpq_document.products[].product_id` | number |  |
| `cpq_document.products[].quantity` | number |  |
| `cpq_document.products[].setup_fee` | number |  |
| `cpq_document.products[].unit_price` | number |  |
| `cpq_document.sales_account_id` | number |  |
| `cpq_document.signing_order_modified` | boolean |  |
| `cpq_document.stage` | string |  |
| `cpq_document.updated_at` | date |  |
| `cpq_document.updater_id` | number |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `PUT /api/cpq/cpq_documents/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/manage-document-products.md) for the provider-specific parameters and requirements.

