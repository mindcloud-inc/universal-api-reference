# Create Quote Template with Simplicate

## Endpoint

- **Method:** `POST`
- **Path:** `/sales/quote`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Create Quote Template](https://developer.simplicate.com/docs/api/v2/reference/create-sales-quote/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_reference` | body | `string` | no | The customer reference |
| `quote_subject` | body | `string` | no | The quote subject |
| `quotetemplate_id` | body | `string` | no | The quote template id |
| `sales_id` | body | `string` | no | The sale id for the quote template |
