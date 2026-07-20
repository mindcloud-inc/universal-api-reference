# Shippo - Legacy: Create Shipment

Creates a new shipment in Shippo.

```
POST https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippo - Legacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `carrier_accounts[]` | array<string> | no |  |
| `customs_declaration.certify_signer` | string | no |  |
| `customs_declaration.contents_explanation` | string | no |  |
| `customs_declaration.contents_type` | string | no |  |
| `customs_declaration.incoterm` | string | no |  |
| `customs_declaration.items[]` | array | no |  |
| `customs_declaration.items[].mass_unit` | string | no |  |
| `customs_declaration.items[].net_weight` | number | no |  |
| `customs_declaration.items[].origin_country` | string | no |  |
| `customs_declaration.items[].quantity` | number | no |  |
| `customs_declaration.items[].sku_code` | string | no |  |
| `customs_declaration.items[].tariff_number` | string | no |  |
| `customs_declaration.items[].value_amount` | number | no |  |
| `customs_declaration.items[].value_currency` | string | no |  |
| `customs_declaration.test` | boolean | no |  |
| `extra.billing.country` | string | no |  |
| `extra.billing.participationCode` | string | no |  |
| `extra.billing.type` | string | no |  |
| `extra.billing.zip` | string | no |  |
| `extra.dangerous_goods.biological_material` | object | no |  |
| `extra.dry_ice` | object | no |  |
| `extra.insurance` | object | no |  |
| `extra.insurance.content` | string | no |  |
| `extra.insurance.currency` | string | no |  |
| `extra.insurance.provider` | string | no |  |
| `extra.is_return` | boolean | no |  |
| `extra.reference_1` | string | no |  |
| `extra.reference_2` | string | no |  |
| `extra.saturday_delivery` | boolean | no |  |
| `extra.signature_confirmation` | string | no |  |
| `address_from` | object | no |  |
| `address_from.name` | string | no |  |
| `address_return.city` | string | no |  |
| `address_to.name` | string | no |  |
| `customs_declaration.certify` | boolean | no |  |
| `customs_declaration.items[].description` | string | no |  |
| `extra.billing.account` | string | no |  |
| `extra.dangerous_goods.biological_material.contains` | boolean | no |  |
| `extra.dangerous_goods.contains` | boolean | no |  |
| `extra.dangerous_goods.lithium_batteries.contains` | boolean | no |  |
| `extra.insurance.amount` | string | no |  |
| `parcels[].extra` | object | no |  |
| `parcels[].extra.COD` | object | no |  |
| `parcels[].extra.COD.amount` | string | no |  |
| `parcels[].extra.insurance.amount` | string | no |  |
| `address_from.company` | string | no |  |
| `address_return` | object | no |  |
| `address_return.state` | string | no |  |
| `address_to.company` | string | no |  |
| `parcels[].extra.COD.currency` | string | no |  |
| `parcels[].extra.insurance` | object | no |  |
| `parcels[].extra.insurance.content` | string | no |  |
| `parcels[].metadata` | string | no |  |
| `address_from.street1` | string | no |  |
| `address_return.name` | string | no |  |
| `address_to` | object | no |  |
| `address_to.street1` | string | no |  |
| `extra.dangerous_goods.lithium_batteries` | object | no |  |
| `parcels[].extra.COD.payment_method` | string | no |  |
| `parcels[].extra.insurance.currency` | string | no |  |
| `parcels[].extra.reference_1` | string | no |  |
| `parcels[].mass_unit` | string | no |  |
| `address_from.street2` | string | no |  |
| `address_return.company` | string | no |  |
| `address_to.street2` | string | no |  |
| `parcels[]` | array | no |  |
| `parcels[].extra.insurance.provider` | string | no |  |
| `parcels[].extra.reference_2` | string | no |  |
| `parcels[].weight` | string | no |  |
| `address_from.street_no` | string | no |  |
| `address_return.street1` | string | no |  |
| `address_to.street_no` | string | no |  |
| `extra` | object | no |  |
| `extra.bypass_address_validation` | boolean | no |  |
| `extra.dangerous_goods` | object | no |  |
| `parcels[].distance_unit` | string | no |  |
| `address_from.city` | string | no |  |
| `address_return.street2` | string | no |  |
| `address_to.city` | string | no |  |
| `customs_declaration` | object | no |  |
| `extra.shipment_date` | string | no |  |
| `parcels[].height` | string | no |  |
| `address_from.state` | string | no |  |
| `address_return.street_no` | string | no |  |
| `address_to.state` | string | no |  |
| `async` | boolean | no |  |
| `parcels[].length` | string | no |  |
| `address_from.zip` | string | no |  |
| `address_return.zip` | string | no |  |
| `address_to.zip` | string | no |  |
| `customs_declaration.non_delivery_option` | string | no |  |
| `extra.dangerous_goods_code` | string | no |  |
| `parcels[].width` | string | no |  |
| `address_from.country` | string | no |  |
| `address_return.country` | string | no |  |
| `address_to.country` | string | no |  |
| `customs_declaration.eel_pfc` | string | no |  |
| `parcels[].template` | string | no |  |
| `address_from.phone` | string | no |  |
| `address_return.phone` | string | no |  |
| `address_to.phone` | string | no |  |
| `customs_declaration.aes_itn` | string | no |  |
| `address_from.email` | string | no |  |
| `address_return.email` | string | no |  |
| `address_to.email` | string | no |  |
| `customs_declaration.b13a_filing_option` | string | no |  |
| `address_from.is_residential` | boolean | no |  |
| `address_return.is_residential` | boolean | no |  |
| `address_to.is_residential` | boolean | no |  |
| `customs_declaration.b13a_number` | string | no |  |
| `extra.billing` | object | no |  |
| `address_from.metadata` | string | no |  |
| `address_return.metadata` | string | no |  |
| `address_to.metadata` | string | no |  |
| `address_from.validate` | boolean | no |  |
| `address_return.validate` | boolean | no |  |
| `address_to.validate` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | no | Override the authentication API key here |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shippo - Legacy API returns.

## Native endpoint

Through the native Shippo - Legacy API, this operation is `POST /shipments` (base URL `https://api.goshippo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

