# Campfire: List Chart Entities

Retrieves chart entities from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/list-chart-entities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "address_1": "string",
      "address_2": "string",
      "business_category": "string",
      "business_type": "string",
      "city": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "disable_service_date": true,
      "elimination_entity": 1,
      "enable_mid_month_convention": true,
      "fiscal_year_day": 1,
      "fiscal_year_month": 1,
      "id": 1,
      "invoice_address": "string",
      "invoice_cc_emails": "ava@example.com",
      "invoice_display_settings": {},
      "invoice_email": "ava@example.com",
      "invoice_email_attachments": [
        {}
      ],
      "invoice_email_body": "ava@example.com",
      "invoice_email_subject": "ava@example.com",
      "invoice_message": "string",
      "invoice_name": "Ava Chen",
      "invoice_prefix": "string",
      "is_deleted": true,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "lineage_array": [
        "string"
      ],
      "logo_url": "https://example.com",
      "mid_month_threshold": 1,
      "name": "Ava Chen",
      "parent": 1,
      "parent_name": "Ava Chen",
      "representative_name": "Ava Chen",
      "state": "string",
      "tax_identification_number": "string",
      "use_whole_month_accounting_for_prepaids": true,
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address_1` | string |  |
| `address_2` | string |  |
| `business_category` | string |  |
| `business_type` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `description` | string |  |
| `disable_service_date` | boolean |  |
| `elimination_entity` | number |  |
| `enable_mid_month_convention` | boolean |  |
| `fiscal_year_day` | number |  |
| `fiscal_year_month` | number |  |
| `id` | number |  |
| `invoice_address` | string |  |
| `invoice_cc_emails` | string |  |
| `invoice_display_settings` | object |  |
| `invoice_email` | string |  |
| `invoice_email_attachments` | array<object> |  |
| `invoice_email_body` | string |  |
| `invoice_email_subject` | string |  |
| `invoice_message` | string |  |
| `invoice_name` | string |  |
| `invoice_prefix` | string |  |
| `is_deleted` | boolean |  |
| `last_modified_at` | date |  |
| `lineage_array` | array<string> |  |
| `logo_url` | string |  |
| `mid_month_threshold` | number |  |
| `name` | string |  |
| `parent` | number |  |
| `parent_name` | string |  |
| `representative_name` | string |  |
| `state` | string |  |
| `tax_identification_number` | string |  |
| `use_whole_month_accounting_for_prepaids` | boolean |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/entity` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chart-entities.md) for the provider-specific parameters and requirements.

