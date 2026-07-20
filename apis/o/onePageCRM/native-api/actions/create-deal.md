# Create Deal with OnePageCRM

Creates a new deal in OnePageCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/deals`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Create Deal](https://developer.onepagecrm.com/api/#/Deals/post_deals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `list<string>` | yes | ID of the contact the deal belongs to |
| `owner_id` | body | `list<string>` | yes | ID of the user who owns the deal |
| `name` | body | `string` | yes | Name of the deal |
| `pipeline_id` | body | `list<string>` | no | ID of the pipeline the deal belongs to |
| `sales_pipeline_id` | body | `list<string>` | no | ID of the sales pipeline the deal belongs to |
| `status` | body | `list<string>` | no | Status of the deal Accepted values: `lost`, `pending`, `won`. |
| `stage` | body | `number` | no | Progress stage for a pending deal |
| `expected_close_date` | body | `string` | no | Date the deal is expected to close in YYYY-MM-DD format. |
| `close_date` | body | `string` | no | Date the deal actually closed in YYYY-MM-DD format. |
| `date` | body | `string` | no | Creation date of the deal in YYYY-MM-DD format. |
| `amount` | body | `number` | no | Monetary value of the deal |
| `months` | body | `number` | no | Number of months for a multi-month deal |
| `cost` | body | `number` | no | Monetary cost of the deal |
| `commission_base` | body | `list<string>` | no | Base used to calculate the commission Accepted values: `amount`, `margin`. |
| `commission_type` | body | `list<string>` | no | Type of commission for the deal Accepted values: `absolute`, `none`, `percentage`. |
| `commission` | body | `number` | no | Commission payable for the deal |
| `commission_percentage` | body | `number` | no | Commission percentage for the deal |
| `text` | body | `string` | no | Extra notes related to the deal |
| `has_deal_items` | body | `boolean` | no | Set to true to create or keep deal items |
| `deal_items[].name` | body | `string` | no | Name of the deal item |
| `deal_items[].description` | body | `string` | no | Description of the deal item |
| `deal_items[].cost` | body | `number` | no | Cost of the deal item |
| `deal_items[].price` | body | `number` | no | Price of the deal item |
| `deal_items[].qty` | body | `number` | no | Quantity of the deal item |
| `deal_items[].predefined_item_id` | body | `string` | no | ID of the predefined item used for deal item creation |
| `deal_fields[].deal_field.id` | body | `string` | no | ID of the deal custom field to set |
| `deal_fields[].value` | body | `string` | no | Value for the deal custom field |
