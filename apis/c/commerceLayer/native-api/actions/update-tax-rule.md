# Update Tax Rule with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/tax_rules/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Tax Rule](https://docs.commercelayer.io/core-api-reference/tax_rules/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The tax rule ID to update. |
| `data.id` | body | `string` | yes | Use the same tax rule ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated tax rule name. |
| `data.attributes.tax_rate` | body | `number` | no | The updated tax rate. |
| `data.attributes.country_code_regex` | body | `string` | no | The updated country code matching regex. |
| `data.attributes.state_code_regex` | body | `string` | no | The updated state code matching regex. |
| `data.attributes.zip_code_regex` | body | `string` | no | The updated zip code matching regex. |
| `data.attributes.freight_taxable` | body | `boolean` | no | Whether freight is taxable under this rule. |
| `data.attributes.payment_method_taxable` | body | `boolean` | no | Whether payment methods are taxable under this rule. |
| `data.attributes.gift_card_taxable` | body | `boolean` | no | Whether gift cards are taxable under this rule. |
| `data.attributes.adjustment_taxable` | body | `boolean` | no | Whether adjustments are taxable under this rule. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
