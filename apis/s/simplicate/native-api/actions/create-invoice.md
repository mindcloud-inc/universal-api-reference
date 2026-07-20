# Create Invoice with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/invoice`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Invoice](https://developer.simplicate.com/docs/api/v2/reference/create-invoices-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | no | Invoice date in YYYY-MM-DD format. |
| `my_organization_profile_id` | body | `string` | no | My organization profile identifier. |
| `organization_id` | body | `string` | no | Invoice recipient organization identifier. |
| `payment_term_id` | body | `string` | no | Payment term identifier. |
| `status_id` | body | `string` | no | Invoice status identifier. |
| `subject` | body | `string` | no | Invoice subject. |
| `invoice_lines` | body | `list<object>` | yes | Array of invoice line objects. |
