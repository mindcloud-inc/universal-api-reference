# Update Deal with OnePageCRM

Updates an existing deal in OnePageCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deals/:deal_id`
- **Base URL:** `https://app.onepagecrm.com/api/v3`
- **Official documentation:** [Update Deal](https://developer.onepagecrm.com/api/#/Deals/put_deals__deal_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `list<string>` | yes | ID of the deal to update |
| `name` | body | `string` | no | Updated deal name |
| `text` | body | `string` | no | Updated notes related to the deal |
| `status` | body | `list<string>` | no | Updated status of the deal Accepted values: `lost`, `pending`, `won`. |
| `stage` | body | `number` | no | Updated progress stage for a pending deal |
| `contact_id` | body | `list<string>` | no | ID of the contact the deal belongs to |
| `owner_id` | body | `list<string>` | no | ID of the user who owns the deal |
| `pipeline_id` | body | `list<string>` | no | ID of the pipeline the deal belongs to |
| `sales_pipeline_id` | body | `list<string>` | no | ID of the sales pipeline the deal belongs to |
| `expected_close_date` | body | `string` | no | Updated expected close date in YYYY-MM-DD format. |
| `close_date` | body | `string` | no | Updated close date in YYYY-MM-DD format. |
| `date` | body | `string` | no | Updated creation date of the deal in YYYY-MM-DD format. |
| `amount` | body | `number` | no | Updated monetary value of the deal |
| `months` | body | `number` | no | Updated number of months for a multi-month deal |
| `cost` | body | `number` | no | Updated monetary cost of the deal |
| `commission_base` | body | `list<string>` | no | Updated base used to calculate the commission Accepted values: `amount`, `margin`. |
| `commission_type` | body | `list<string>` | no | Updated type of commission for the deal Accepted values: `absolute`, `none`, `percentage`. |
| `commission` | body | `number` | no | Updated commission payable for the deal |
| `commission_percentage` | body | `number` | no | Updated commission percentage for the deal |
| `has_deal_items` | body | `boolean` | no | Set to true to create or keep deal items |
| `deal_items[].name` | body | `string` | no | Name of the deal item |
| `deal_items[].description` | body | `string` | no | Description of the deal item |
| `deal_items[].cost` | body | `number` | no | Cost of the deal item |
| `deal_items[].price` | body | `number` | no | Price of the deal item |
| `deal_items[].qty` | body | `number` | no | Quantity of the deal item |
| `deal_items[].predefined_item_id` | body | `string` | no | ID of the predefined item used for deal item creation |
| `deal_fields[].deal_field.id` | body | `string` | no | ID of the deal custom field to update |
| `deal_fields[].value` | body | `string` | no | Value for the deal custom field |
