# Freshworks CRM: Get Document

Retrieves a document from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-document?${params}`, {
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
| `id` | string | yes |  |

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
        "sales_account_id": 1,
        "signing_order_modified": true,
        "stage": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
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
| `cpq_document.sales_account_id` | number |  |
| `cpq_document.signing_order_modified` | boolean |  |
| `cpq_document.stage` | string |  |
| `cpq_document.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/cpq/cpq_documents/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

