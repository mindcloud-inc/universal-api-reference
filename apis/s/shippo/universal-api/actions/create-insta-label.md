# Shippo - Legacy: Create Insta Label

Creates a shipping label in one Shippo API call.

```
POST https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-insta-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippo - Legacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-insta-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippo/latest/actions/create-insta-label', {
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
| `carrier_account` | string | no |  |
| `label_file_type` | string | no |  |
| `shipment` | object | no |  |
| `shipment.address_from.company` | string | no |  |
| `shipment.address_from.country` | string | no |  |
| `shipment.address_from.email` | string | no |  |
| `shipment.address_from.is_residential` | boolean | no |  |
| `shipment.address_from.name` | string | no |  |
| `shipment.address_from.phone` | string | no |  |
| `shipment.address_from.state` | string | no |  |
| `shipment.address_from.street1` | string | no |  |
| `shipment.address_from.street2` | string | no |  |
| `shipment.address_from.zip` | string | no |  |
| `shipment.address_return.company` | string | no |  |
| `shipment.address_return.country` | string | no |  |
| `shipment.address_return.email` | string | no |  |
| `shipment.address_return.is_residential` | boolean | no |  |
| `shipment.address_return.metadata` | string | no |  |
| `shipment.address_return.name` | string | no |  |
| `shipment.address_return.phone` | string | no |  |
| `shipment.address_return.state` | string | no |  |
| `shipment.address_return.street1` | string | no |  |
| `shipment.address_return.street2` | string | no |  |
| `shipment.address_return.validate` | boolean | no |  |
| `shipment.address_return.zip` | string | no |  |
| `shipment.address_to.company` | string | no |  |
| `shipment.address_to.country` | string | no |  |
| `shipment.address_to.email` | string | no |  |
| `shipment.address_to.is_residential` | boolean | no |  |
| `shipment.address_to.name` | string | no |  |
| `shipment.address_to.phone` | string | no |  |
| `shipment.address_to.state` | string | no |  |
| `shipment.address_to.street1` | string | no |  |
| `shipment.address_to.street2` | string | no |  |
| `shipment.address_to.zip` | string | no |  |
| `shipment.extra.dangerous_goods.biological_material` | object | no |  |
| `shipment.extra.insurance.content` | string | no |  |
| `shipment.extra.insurance.currency` | string | no |  |
| `shipment.extra.insurance.provider` | string | no |  |
| `shipment.extra.saturday_delivery` | boolean | no |  |
| `shipment.parcels[].length` | string | no |  |
| `async` | boolean | no |  |
| `shipment.address_from` | object | no |  |
| `shipment.address_from.city` | string | no |  |
| `shipment.address_return.city` | string | no |  |
| `shipment.address_to.city` | string | no |  |
| `shipment.customs_declaration.certify` | boolean | no |  |
| `shipment.customs_declaration.items[].description` | string | no |  |
| `shipment.extra.billing.account` | string | no |  |
| `shipment.extra.bypass_address_validation` | boolean | no |  |
| `shipment.extra.dangerous_goods.biological_material.contains` | boolean | no |  |
| `shipment.extra.dangerous_goods.contains` | boolean | no |  |
| `shipment.extra.dangerous_goods.lithium_batteries.contains` | boolean | no |  |
| `shipment.extra.dry_ice.contains_dry_ice` | boolean | no |  |
| `shipment.extra.insurance.amount` | string | no |  |
| `shipment.parcels[].distance_unit` | string | no |  |
| `shipment.parcels[].extra.insurance` | object | no |  |
| `shipment.parcels[].extra.insurance.amount` | string | no |  |
| `shipment.address_return` | object | no |  |
| `shipment.customs_declaration.certify_signer` | string | no |  |
| `shipment.customs_declaration.items[].mass_unit` | string | no |  |
| `shipment.extra.billing.country` | string | no |  |
| `shipment.extra.dry_ice` | object | no |  |
| `shipment.extra.dry_ice.weight` | string | no |  |
| `shipment.parcels[].extra.insurance.content` | string | no |  |
| `shipment.parcels[].height` | string | no |  |
| `shipment.address_to` | object | no |  |
| `shipment.customs_declaration.contents_explanation` | string | no |  |
| `shipment.customs_declaration.items[].net_weight` | number | no |  |
| `shipment.extra.billing.participation_code` | string | no |  |
| `shipment.extra.dangerous_goods.lithium_batteries` | object | no |  |
| `shipment.extra.is_return` | boolean | no |  |
| `shipment.parcels[].extra.insurance.currency` | string | no |  |
| `servicelevel_token` | string | no |  |
| `shipment.customs_declaration` | object | no |  |
| `shipment.customs_declaration.contents_type` | string | no |  |
| `shipment.customs_declaration.items[].origin_country` | string | no |  |
| `shipment.extra.billing.type` | string | no |  |
| `shipment.extra.reference_1` | string | no |  |
| `shipment.parcels[].extra.insurance.provider` | string | no |  |
| `shipment.parcels[].width` | string | no |  |
| `shipment.customs_declaration.incoterm` | string | no |  |
| `shipment.customs_declaration.items[].quantity` | number | no |  |
| `shipment.extra` | object | no |  |
| `shipment.extra.billing.zip` | string | no |  |
| `shipment.extra.reference_2` | string | no |  |
| `shipment.parcels[].mass_unit` | string | no |  |
| `shipment.customs_declaration.items[]` | array | no |  |
| `shipment.customs_declaration.items[].sku_code` | string | no |  |
| `shipment.parcels[]` | array | no |  |
| `shipment.parcels[].weight` | string | no |  |
| `shipment.customs_declaration.eel_pfc` | string | no |  |
| `shipment.customs_declaration.items[].tariff_number` | string | no |  |
| `shipment.extra.signature_confirmation` | string | no |  |
| `shipment.parcels[].template` | string | no |  |
| `shipment.shipment_date` | string | no |  |
| `shipment.customs_declaration.aes_itn` | string | no |  |
| `shipment.customs_declaration.test` | boolean | no |  |
| `shipment.extra.dangerous_goods` | object | no |  |
| `shipment.parcels[].metadata` | string | no |  |
| `shipment.customs_declaration.items[].value_amount` | number | no |  |
| `shipment.extra.insurance` | object | no |  |
| `shipment.parcels[].extra` | object | no |  |
| `shipment.customs_declaration.items[].value_currency` | string | no |  |
| `shipment.customs_declaration.non_delivery_option` | string | no |  |
| `shipment.extra.dangerous_goods_code` | string | no |  |
| `shipment.customs_declaration.b13a_filing_option` | string | no |  |
| `shipment.extra.billing` | object | no |  |
| `shipment.customs_declaration.b13a_number` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | no | Override the authentication API key here |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commercialInvoiceUrl": {},
      "createdBy": {},
      "eta": {},
      "labelUrl": "https://example.com",
      "metadata": "string",
      "objectCreated": "string",
      "objectId": "string",
      "objectOwner": "string",
      "objectState": "string",
      "objectUpdated": "string",
      "order": {},
      "parcel": "string",
      "qrCodeUrl": {},
      "rate": {
        "amount": "string",
        "amountLocal": "string",
        "carrierAccount": "string",
        "currency": "string",
        "currencyLocal": "string",
        "objectId": "string",
        "provider": "string",
        "servicelevelName": "Ava Chen",
        "servicelevelToken": "string"
      },
      "status": "string",
      "test": true,
      "trackingNumber": "string",
      "trackingStatus": "string",
      "trackingUrlProvider": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commercialInvoiceUrl` | object |  |
| `createdBy` | object |  |
| `eta` | object |  |
| `labelUrl` | string |  |
| `metadata` | string |  |
| `objectCreated` | string |  |
| `objectId` | string |  |
| `objectOwner` | string |  |
| `objectState` | string |  |
| `objectUpdated` | string |  |
| `order` | object |  |
| `parcel` | string |  |
| `qrCodeUrl` | object |  |
| `rate.amount` | string |  |
| `rate.amountLocal` | string |  |
| `rate.carrierAccount` | string |  |
| `rate.currency` | string |  |
| `rate.currencyLocal` | string |  |
| `rate.objectId` | string |  |
| `rate.provider` | string |  |
| `rate.servicelevelName` | string |  |
| `rate.servicelevelToken` | string |  |
| `status` | string |  |
| `test` | boolean |  |
| `trackingNumber` | string |  |
| `trackingStatus` | string |  |
| `trackingUrlProvider` | string |  |

## Native endpoint

Through the native Shippo - Legacy API, this operation is `POST /transactions/` (base URL `https://api.goshippo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-insta-label.md) for the provider-specific parameters and requirements.

