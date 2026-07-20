# Create Tax Rule with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/tax_rules`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Tax Rule](https://docs.commercelayer.io/core-api-reference/tax_rules/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The tax rule name. |
| `data.attributes.tax_rate` | body | `number` | yes | The tax rate applied by this rule. |
| `data.attributes.country_code_regex` | body | `string` | no | A regular expression matching shipping address country codes. |
| `data.attributes.state_code_regex` | body | `string` | no | A regular expression matching shipping address state codes. |
| `data.attributes.zip_code_regex` | body | `string` | no | A regular expression matching shipping address zip codes. |
| `data.attributes.freight_taxable` | body | `boolean` | no | Whether freight is taxable under this rule. |
| `data.attributes.payment_method_taxable` | body | `boolean` | no | Whether payment methods are taxable under this rule. |
| `data.attributes.gift_card_taxable` | body | `boolean` | no | Whether gift cards are taxable under this rule. |
| `data.attributes.adjustment_taxable` | body | `boolean` | no | Whether adjustments are taxable under this rule. |
| `data.attributes.reference` | body | `string` | no | An external reference for the tax rule. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
| `data.relationships.manual_tax_calculator.data.id` | body | `string` | yes | The ID of the manual tax calculator to link to this tax rule. |
