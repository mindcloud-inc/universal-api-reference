# Update Customer with Booqable

Updates an existing customer in Booqable.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/:id`
- **Base URL:** `https://mindcloud.booqable.com/api/4`
- **Official documentation:** [Update Customer](https://developers.booqable.com/#customers-update-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Customer ID. |
| `fields[customers]` | query | `string` | no | Comma-separated customer fields to include instead of the default field set. |
| `include` | query | `string` | no | Comma-separated relationships to sideload. |
| `data[attributes][name]` | body | `string` | no | Person or company name. |
| `data[attributes][email]` | body | `string` | no | Email address used for communication. |
| `data[attributes][legal_type]` | body | `string` | no | Whether the customer is a person or commercial entity. |
| `data[attributes][deposit_type]` | body | `string` | no | Default deposit type for new orders. |
| `data[attributes][deposit_value]` | body | `number` | no | Deposit value used with the selected deposit type. |
| `data[attributes][discount_percentage]` | body | `number` | no | Default discount applied to new orders for this customer. |
| `data[attributes][email_marketing_consented]` | body | `boolean` | no | Whether the customer has consented to receive email marketing. |
| `data[attributes][merge_suggestion_customer_id]` | body | `string` | no | Customer this record may duplicate. |
| `data[attributes][stripe_id]` | body | `string` | no | Stripe customer ID. |
| `data[attributes][tag_list][]` | body | `array<string>` | no | Case-insensitive customer tags. |
| `data[attributes][tax_region_id]` | body | `string` | no | Tax region for new orders for this customer. |
