# Campfire Universal API Examples

These examples use the MindCloud API key and Campfire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Chart Entities

Retrieves chart entities from Campfire.

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

Example response:

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

See the full [List Chart Entities action reference](actions/list-chart-entities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campfire/latest/actions/list-chart-entities).
