# Create Insta Label with Shippo - Legacy

Creates a shipping label in one Shippo API call.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/`
- **Base URL:** `https://api.goshippo.com`
- **Official documentation:** [Create Insta Label](https://docs.goshippo.com/docs/guides_general/single_call/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrier_account` | body | `string` | no | — |
| `label_file_type` | body | `string` | no | — |
| `shipment` | body | `object` | no | — |
| `shipment.address_from.company` | body | `string` | no | — |
| `shipment.address_from.country` | body | `string` | no | — |
| `shipment.address_from.email` | body | `string` | no | — |
| `shipment.address_from.is_residential` | body | `boolean` | no | — |
| `shipment.address_from.name` | body | `string` | no | — |
| `shipment.address_from.phone` | body | `string` | no | — |
| `shipment.address_from.state` | body | `string` | no | — |
| `shipment.address_from.street1` | body | `string` | no | — |
| `shipment.address_from.street2` | body | `string` | no | — |
| `shipment.address_from.zip` | body | `string` | no | — |
| `shipment.address_return.company` | body | `string` | no | — |
| `shipment.address_return.country` | body | `string` | no | — |
| `shipment.address_return.email` | body | `string` | no | — |
| `shipment.address_return.is_residential` | body | `boolean` | no | — |
| `shipment.address_return.metadata` | body | `string` | no | — |
| `shipment.address_return.name` | body | `string` | no | — |
| `shipment.address_return.phone` | body | `string` | no | — |
| `shipment.address_return.state` | body | `string` | no | — |
| `shipment.address_return.street1` | body | `string` | no | — |
| `shipment.address_return.street2` | body | `string` | no | — |
| `shipment.address_return.validate` | body | `boolean` | no | — |
| `shipment.address_return.zip` | body | `string` | no | — |
| `shipment.address_to.company` | body | `string` | no | — |
| `shipment.address_to.country` | body | `string` | no | — |
| `shipment.address_to.email` | body | `string` | no | — |
| `shipment.address_to.is_residential` | body | `boolean` | no | — |
| `shipment.address_to.name` | body | `string` | no | — |
| `shipment.address_to.phone` | body | `string` | no | — |
| `shipment.address_to.state` | body | `string` | no | — |
| `shipment.address_to.street1` | body | `string` | no | — |
| `shipment.address_to.street2` | body | `string` | no | — |
| `shipment.address_to.zip` | body | `string` | no | — |
| `shipment.extra.dangerous_goods.biological_material` | body | `object` | no | — |
| `shipment.extra.insurance.content` | body | `string` | no | — |
| `shipment.extra.insurance.currency` | body | `string` | no | — |
| `shipment.extra.insurance.provider` | body | `string` | no | — |
| `shipment.extra.saturday_delivery` | body | `boolean` | no | — |
| `shipment.parcels[].length` | body | `string` | no | — |
| `async` | body | `boolean` | no | — |
| `shipment.address_from` | body | `object` | no | — |
| `shipment.address_from.city` | body | `string` | no | — |
| `shipment.address_return.city` | body | `string` | no | — |
| `shipment.address_to.city` | body | `string` | no | — |
| `shipment.customs_declaration.certify` | body | `boolean` | no | — |
| `shipment.customs_declaration.items[].description` | body | `string` | no | — |
| `shipment.extra.billing.account` | body | `string` | no | — |
| `shipment.extra.bypass_address_validation` | body | `boolean` | no | — |
| `shipment.extra.dangerous_goods.biological_material.contains` | body | `boolean` | no | — |
| `shipment.extra.dangerous_goods.contains` | body | `boolean` | no | — |
| `shipment.extra.dangerous_goods.lithium_batteries.contains` | body | `boolean` | no | — |
| `shipment.extra.dry_ice.contains_dry_ice` | body | `boolean` | no | — |
| `shipment.extra.insurance.amount` | body | `string` | no | — |
| `shipment.parcels[].distance_unit` | body | `string` | no | — |
| `shipment.parcels[].extra.insurance` | body | `object` | no | — |
| `shipment.parcels[].extra.insurance.amount` | body | `string` | no | — |
| `shipment.address_return` | body | `object` | no | — |
| `shipment.customs_declaration.certify_signer` | body | `string` | no | — |
| `shipment.customs_declaration.items[].mass_unit` | body | `string` | no | — |
| `shipment.extra.billing.country` | body | `string` | no | — |
| `shipment.extra.dry_ice` | body | `object` | no | — |
| `shipment.extra.dry_ice.weight` | body | `string` | no | — |
| `shipment.parcels[].extra.insurance.content` | body | `string` | no | — |
| `shipment.parcels[].height` | body | `string` | no | — |
| `shipment.address_to` | body | `object` | no | — |
| `shipment.customs_declaration.contents_explanation` | body | `string` | no | — |
| `shipment.customs_declaration.items[].net_weight` | body | `number` | no | — |
| `shipment.extra.billing.participation_code` | body | `string` | no | — |
| `shipment.extra.dangerous_goods.lithium_batteries` | body | `object` | no | — |
| `shipment.extra.is_return` | body | `boolean` | no | — |
| `shipment.parcels[].extra.insurance.currency` | body | `string` | no | — |
| `servicelevel_token` | body | `string` | no | — |
| `shipment.customs_declaration` | body | `object` | no | — |
| `shipment.customs_declaration.contents_type` | body | `string` | no | — |
| `shipment.customs_declaration.items[].origin_country` | body | `string` | no | — |
| `shipment.extra.billing.type` | body | `string` | no | — |
| `shipment.extra.reference_1` | body | `string` | no | — |
| `shipment.parcels[].extra.insurance.provider` | body | `string` | no | — |
| `shipment.parcels[].width` | body | `string` | no | — |
| `shipment.customs_declaration.incoterm` | body | `string` | no | — |
| `shipment.customs_declaration.items[].quantity` | body | `number` | no | — |
| `shipment.extra` | body | `object` | no | — |
| `shipment.extra.billing.zip` | body | `string` | no | — |
| `shipment.extra.reference_2` | body | `string` | no | — |
| `shipment.parcels[].mass_unit` | body | `string` | no | — |
| `apiKey` | path | `string` | no | Override the authentication API key here |
| `shipment.customs_declaration.items[]` | body | `array` | no | — |
| `shipment.customs_declaration.items[].sku_code` | body | `string` | no | — |
| `shipment.parcels[]` | body | `array` | no | — |
| `shipment.parcels[].weight` | body | `string` | no | — |
| `shipment.customs_declaration.eel_pfc` | body | `string` | no | — |
| `shipment.customs_declaration.items[].tariff_number` | body | `string` | no | — |
| `shipment.extra.signature_confirmation` | body | `string` | no | — |
| `shipment.parcels[].template` | body | `string` | no | — |
| `shipment.shipment_date` | body | `string` | no | — |
| `shipment.customs_declaration.aes_itn` | body | `string` | no | — |
| `shipment.customs_declaration.test` | body | `boolean` | no | — |
| `shipment.extra.dangerous_goods` | body | `object` | no | — |
| `shipment.parcels[].metadata` | body | `string` | no | — |
| `shipment.customs_declaration.items[].value_amount` | body | `number` | no | — |
| `shipment.extra.insurance` | body | `object` | no | — |
| `shipment.parcels[].extra` | body | `object` | no | — |
| `shipment.customs_declaration.items[].value_currency` | body | `string` | no | — |
| `shipment.customs_declaration.non_delivery_option` | body | `string` | no | — |
| `shipment.extra.dangerous_goods_code` | body | `string` | no | — |
| `shipment.customs_declaration.b13a_filing_option` | body | `string` | no | — |
| `shipment.extra.billing` | body | `object` | no | — |
| `shipment.customs_declaration.b13a_number` | body | `string` | no | — |
