# Create Shipment with Shippo - Legacy

Creates a new shipment in Shippo.

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments`
- **Base URL:** `https://api.goshippo.com`
- **Official documentation:** [Create Shipment](https://docs.goshippo.com/shippoapi/public-api/#operation/CreateShipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `carrier_accounts[]` | body | `array<string>` | no | — |
| `customs_declaration.certify_signer` | body | `string` | no | — |
| `customs_declaration.contents_explanation` | body | `string` | no | — |
| `customs_declaration.contents_type` | body | `string` | no | — |
| `customs_declaration.incoterm` | body | `string` | no | — |
| `customs_declaration.items[]` | body | `array` | no | — |
| `customs_declaration.items[].mass_unit` | body | `string` | no | — |
| `customs_declaration.items[].net_weight` | body | `number` | no | — |
| `customs_declaration.items[].origin_country` | body | `string` | no | — |
| `customs_declaration.items[].quantity` | body | `number` | no | — |
| `customs_declaration.items[].sku_code` | body | `string` | no | — |
| `customs_declaration.items[].tariff_number` | body | `string` | no | — |
| `customs_declaration.items[].value_amount` | body | `number` | no | — |
| `customs_declaration.items[].value_currency` | body | `string` | no | — |
| `customs_declaration.test` | body | `boolean` | no | — |
| `extra.billing.country` | body | `string` | no | — |
| `extra.billing.participationCode` | body | `string` | no | — |
| `extra.billing.type` | body | `string` | no | — |
| `extra.billing.zip` | body | `string` | no | — |
| `extra.dangerous_goods.biological_material` | body | `object` | no | — |
| `extra.dry_ice` | body | `object` | no | — |
| `extra.insurance` | body | `object` | no | — |
| `extra.insurance.content` | body | `string` | no | — |
| `extra.insurance.currency` | body | `string` | no | — |
| `extra.insurance.provider` | body | `string` | no | — |
| `extra.is_return` | body | `boolean` | no | — |
| `extra.reference_1` | body | `string` | no | — |
| `extra.reference_2` | body | `string` | no | — |
| `extra.saturday_delivery` | body | `boolean` | no | — |
| `extra.signature_confirmation` | body | `string` | no | — |
| `address_from` | body | `object` | no | — |
| `address_from.name` | body | `string` | no | — |
| `address_return.city` | body | `string` | no | — |
| `address_to.name` | body | `string` | no | — |
| `customs_declaration.certify` | body | `boolean` | no | — |
| `customs_declaration.items[].description` | body | `string` | no | — |
| `extra.billing.account` | body | `string` | no | — |
| `extra.dangerous_goods.biological_material.contains` | body | `boolean` | no | — |
| `extra.dangerous_goods.contains` | body | `boolean` | no | — |
| `extra.dangerous_goods.lithium_batteries.contains` | body | `boolean` | no | — |
| `extra.insurance.amount` | body | `string` | no | — |
| `parcels[].extra` | body | `object` | no | — |
| `parcels[].extra.COD` | body | `object` | no | — |
| `parcels[].extra.COD.amount` | body | `string` | no | — |
| `parcels[].extra.insurance.amount` | body | `string` | no | — |
| `address_from.company` | body | `string` | no | — |
| `address_return` | body | `object` | no | — |
| `address_return.state` | body | `string` | no | — |
| `address_to.company` | body | `string` | no | — |
| `parcels[].extra.COD.currency` | body | `string` | no | — |
| `parcels[].extra.insurance` | body | `object` | no | — |
| `parcels[].extra.insurance.content` | body | `string` | no | — |
| `parcels[].metadata` | body | `string` | no | — |
| `address_from.street1` | body | `string` | no | — |
| `address_return.name` | body | `string` | no | — |
| `address_to` | body | `object` | no | — |
| `address_to.street1` | body | `string` | no | — |
| `extra.dangerous_goods.lithium_batteries` | body | `object` | no | — |
| `parcels[].extra.COD.payment_method` | body | `string` | no | — |
| `parcels[].extra.insurance.currency` | body | `string` | no | — |
| `parcels[].extra.reference_1` | body | `string` | no | — |
| `parcels[].mass_unit` | body | `string` | no | — |
| `address_from.street2` | body | `string` | no | — |
| `address_return.company` | body | `string` | no | — |
| `address_to.street2` | body | `string` | no | — |
| `parcels[]` | body | `array` | no | — |
| `parcels[].extra.insurance.provider` | body | `string` | no | — |
| `parcels[].extra.reference_2` | body | `string` | no | — |
| `parcels[].weight` | body | `string` | no | — |
| `address_from.street_no` | body | `string` | no | — |
| `address_return.street1` | body | `string` | no | — |
| `address_to.street_no` | body | `string` | no | — |
| `extra` | body | `object` | no | — |
| `extra.bypass_address_validation` | body | `boolean` | no | — |
| `extra.dangerous_goods` | body | `object` | no | — |
| `parcels[].distance_unit` | body | `string` | no | — |
| `address_from.city` | body | `string` | no | — |
| `address_return.street2` | body | `string` | no | — |
| `address_to.city` | body | `string` | no | — |
| `customs_declaration` | body | `object` | no | — |
| `extra.shipment_date` | body | `string` | no | — |
| `parcels[].height` | body | `string` | no | — |
| `address_from.state` | body | `string` | no | — |
| `address_return.street_no` | body | `string` | no | — |
| `address_to.state` | body | `string` | no | — |
| `async` | body | `boolean` | no | — |
| `parcels[].length` | body | `string` | no | — |
| `address_from.zip` | body | `string` | no | — |
| `address_return.zip` | body | `string` | no | — |
| `address_to.zip` | body | `string` | no | — |
| `customs_declaration.non_delivery_option` | body | `string` | no | — |
| `extra.dangerous_goods_code` | body | `string` | no | — |
| `parcels[].width` | body | `string` | no | — |
| `address_from.country` | body | `string` | no | — |
| `address_return.country` | body | `string` | no | — |
| `address_to.country` | body | `string` | no | — |
| `apiKey` | path | `string` | no | Override the authentication API key here |
| `customs_declaration.eel_pfc` | body | `string` | no | — |
| `parcels[].template` | body | `string` | no | — |
| `address_from.phone` | body | `string` | no | — |
| `address_return.phone` | body | `string` | no | — |
| `address_to.phone` | body | `string` | no | — |
| `customs_declaration.aes_itn` | body | `string` | no | — |
| `address_from.email` | body | `string` | no | — |
| `address_return.email` | body | `string` | no | — |
| `address_to.email` | body | `string` | no | — |
| `customs_declaration.b13a_filing_option` | body | `string` | no | — |
| `address_from.is_residential` | body | `boolean` | no | — |
| `address_return.is_residential` | body | `boolean` | no | — |
| `address_to.is_residential` | body | `boolean` | no | — |
| `customs_declaration.b13a_number` | body | `string` | no | — |
| `extra.billing` | body | `object` | no | — |
| `address_from.metadata` | body | `string` | no | — |
| `address_return.metadata` | body | `string` | no | — |
| `address_to.metadata` | body | `string` | no | — |
| `address_from.validate` | body | `boolean` | no | — |
| `address_return.validate` | body | `boolean` | no | — |
| `address_to.validate` | body | `boolean` | no | — |
