# Extensiv Order Manager: Create Order

Creates orders in Extensiv Order Manager.

```
POST https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "insuranceCost": {},
  "insuredValue": {},
  "salesChannelId": 1,
  "shipAddress1": "string",
  "shipCity": "string",
  "shipCountry": "string",
  "shipName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "insuranceCost": {},
    "insuredValue": {},
    "salesChannelId": 1,
    "shipAddress1": "string",
    "shipCity": "string",
    "shipCountry": "string",
    "shipName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amountPaid` | object | no |  |
| `amountPaid.amount` | number | no |  |
| `confirmationCost.amount` | number | no |  |
| `customFieldValues[].customFieldDefId` | string | no |  |
| `customsDeclarationItems.country` | string | no |  |
| `customsDeclarationItems.declaredValue.amount` | number | no |  |
| `customShipBilling.accountNumber` | string | no |  |
| `customShipBilling.codAmount.amount` | number | no |  |
| `discount.amount` | number | no |  |
| `insuranceCost.amount` | number | no |  |
| `insuredValue.amount` | number | no |  |
| `orderTotal.amount` | number | no |  |
| `shipMethod.ltlFtlShipment` | object | no |  |
| `shipMethod.ltlFtlShipment.boxCount` | number | no |  |
| `shipMethod.ltlFtlShipment.contact.email` | string | no |  |
| `shipMethod.ltlFtlShipment.pallets[].height` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packages[].height` | number | no |  |
| `shippingCost.amount` | number | no |  |
| `amountPaid.currency` | string | no |  |
| `billDutiesToPayor` | boolean | no |  |
| `confirmationCost.currency` | string | no |  |
| `customsDeclarationItems.declaredValue` | object | no |  |
| `customsDeclarationItems.declaredValue.currency` | string | no |  |
| `customShipBilling.billingZipCode` | string | no |  |
| `customShipBilling.codAmount.currency` | string | no |  |
| `discount.currency` | string | no |  |
| `insuranceCost.currency` | string | no |  |
| `insuredValue.currency` | string | no |  |
| `orderTotal.currency` | string | no |  |
| `shipMethod.ltlFtlShipment.contact` | object | no |  |
| `shipMethod.ltlFtlShipment.contact.fax` | string | no |  |
| `shipMethod.ltlFtlShipment.pallets[].id` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packages[].id` | number | no |  |
| `shipMethod.packageTypeId` | number | no |  |
| `shippingCost.currency` | string | no |  |
| `confirmationCost` | object | no |  |
| `customsDeclarationItems.description` | string | no |  |
| `customShipBilling.codAmount` | object | no |  |
| `shipMethod.ltlFtlShipment.contact.id` | number | no |  |
| `shipMethod.ltlFtlShipment.freightReadyDate` | string | no |  |
| `shipMethod.ltlFtlShipment.pallets[].length` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packages[].length` | number | no |  |
| `shipMethod.shippingCarrier` | string | no |  |
| `containsAlcohol` | boolean | no |  |
| `customsDeclarationItems.harmonizationCode` | string | no |  |
| `customShipBilling.country` | string | no |  |
| `shipMethod.ltlFtlShipment.contact.name` | string | no |  |
| `shipMethod.ltlFtlShipment.id` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packages[].packagingTypeId` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packagingType` | string | no |  |
| `shipMethod.shippingProviderId` | number | no |  |
| `containsDryIce` | boolean | no |  |
| `customsDeclarationItems.productId` | number | no |  |
| `shipMethod.ltlFtlShipment.contact.phone` | string | no |  |
| `shipMethod.ltlFtlShipment.liabilityCoverage` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packages[].width` | number | no |  |
| `shipMethod.ltlFtlShipment.pallets[].width` | number | no |  |
| `shipMethod.shippingServiceId` | number | no |  |
| `customField1` | string | no |  |
| `customsDeclarationItems.quantity` | number | no |  |
| `shipMethod.ltlFtlShipment.liabilityType` | string | no |  |
| `shipMethod.ltlFtlShipment.pallets[].packages[]` | array<object> | no |  |
| `customField2` | string | no |  |
| `customsDeclarationItems.weight` | number | no |  |
| `shipMethod.ltlFtlShipment.measurementUnitId` | number | no |  |
| `customField3` | string | no |  |
| `customsDeclarationItems.weightUnit` | string | no |  |
| `shipMethod.ltlFtlShipment.pallets[]` | array<object> | no |  |
| `customFieldValues[]` | array<object> | no |  |
| `shipMethod.ltlFtlShipment.roleType` | string | no |  |
| `customShipBilling` | object | no |  |
| `shipMethod.ltlFtlShipment.sellerDeclaredValue` | number | no |  |
| `customShipBillingOption` | string | no |  |
| `shipMethod.ltlFtlShipment.sellerFreightClass` | string | no |  |
| `customsDeclarationItems` | object | no |  |
| `shipMethod.ltlFtlShipment.specialService` | string | no |  |
| `customsDeclarationType` | string | no |  |
| `shipMethod.ltlFtlShipment.totalWeight` | number | no |  |
| `deliveryConfirmation` | string | no |  |
| `discount` | object | no |  |
| `doNotPrepayPostage` | boolean | no |  |
| `dryIceWeight` | number | no |  |
| `gift` | boolean | no |  |
| `giftMessage` | string | no |  |
| `height` | number | no |  |
| `holdUntilDate` | string | no |  |
| `includeReturnLabel` | boolean | no |  |
| `insuranceCost` | object | yes |  |
| `insuranceProvider` | string | no |  |
| `insuredValue` | object | yes |  |
| `internalNotes` | string | no |  |
| `length` | number | no |  |
| `nonMachinable` | boolean | no |  |
| `notesFromBuyer` | string | no |  |
| `notesToBuyer` | string | no |  |
| `orderDate` | string | no |  |
| `orderItems[]` | array | no |  |
| `orderNumber` | string | no |  |
| `orderTotal` | object | no |  |
| `paymentDate` | string | no |  |
| `receiveByDate` | string | no |  |
| `releaseWithoutSignature` | boolean | no |  |
| `requestedShippingService` | string | no |  |
| `salesChannelId` | number | yes |  |
| `saturdayDelivery` | boolean | no |  |
| `shipAddress1` | string | yes |  |
| `shipAddress2` | string | no |  |
| `shipAddress3` | string | no |  |
| `shipByDate` | string | no |  |
| `shipCity` | string | yes |  |
| `shipCompany` | string | no |  |
| `shipCountry` | string | yes |  |
| `shipEmail` | string | no |  |
| `shipMethod` | object | no |  |
| `shipName` | string | yes |  |
| `shipPhone` | string | no |  |
| `shipState` | string | no |  |
| `shipZipCode` | string | no |  |
| `shippingCost` | object | no |  |
| `showPostage` | boolean | no |  |
| `suppressChannelUpdate` | boolean | no |  |
| `weight` | number | no |  |
| `width` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
        1
      ],
      "message": "string",
      "orders": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<number> | Created order identifiers. |
| `message` | string | Create order result message. |
| `orders` | array<object> | Created order result records. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `PUT /v1/order` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

