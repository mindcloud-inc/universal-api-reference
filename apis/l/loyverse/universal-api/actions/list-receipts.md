# Loyverse: List Receipts

Retrieves sales receipt records from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-receipts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-receipts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receiptNumbers` | string | no | Return only receipts specified by a comma-separated list of receipt numbers |
| `sinceReceiptNumber` | string | no | Show receipts since date which is equal to created_at date of the receipt with specified number |
| `beforeReceiptNumber` | string | no | Show receipts up to date which is equal to created_at date of the receipt with specified number |
| `storeId` | string | no | Show receipts only for specified store |
| `order` | string | no | Filter receipts by order |
| `source` | string | no | The name of the the source this receipt comes from |
| `updatedAtMin` | date | no | Show receipts updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMax` | date | no | Show receipts updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `createdAtMin` | date | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `createdAtMax` | date | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `limit` | number | no | Used for pagination |
| `cursor` | string | no | Used for pagination |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "receipts": [
        {
          "cancelledAt": "2026-05-07T12:00:00.000Z",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "customerId": "string",
          "diningOption": "string",
          "employeeId": "string",
          "lineItems": [
            {
              "cost": 1,
              "costTotal": 1,
              "grossTotalMoney": 1,
              "id": "string",
              "itemId": "string",
              "itemName": "Ava Chen",
              "lineDiscounts": [
                {
                  "id": "string",
                  "moneyAmount": 1,
                  "name": "Ava Chen",
                  "percentage": 1,
                  "type": "string"
                }
              ],
              "lineModifiers": [
                {
                  "id": "string",
                  "modifierOptionId": "string",
                  "moneyAmount": 1,
                  "name": "Ava Chen",
                  "option": "string",
                  "price": 1
                }
              ],
              "lineNote": "string",
              "lineTaxes": [
                {
                  "id": "string",
                  "moneyAmount": 1,
                  "name": "Ava Chen",
                  "rate": 1,
                  "type": "string"
                }
              ],
              "price": 1,
              "quantity": 1,
              "sku": "string",
              "totalDiscount": 1,
              "totalMoney": 1,
              "variantId": "string",
              "variantName": "Ava Chen"
            }
          ],
          "note": "string",
          "order": "string",
          "payments": [
            {
              "moneyAmount": 1,
              "name": "Ava Chen",
              "paidAt": "2026-05-07T12:00:00.000Z",
              "paymentDetails": {
                "authorizationCode": "string",
                "cardCompany": "string",
                "cardNumber": "string",
                "entryMethod": "string",
                "referenceId": "string"
              },
              "paymentTypeId": "string",
              "type": "string"
            }
          ],
          "pointsBalance": 1,
          "pointsDeducted": 1,
          "pointsEarned": 1,
          "posDeviceId": "string",
          "receiptDate": "2026-05-07T12:00:00.000Z",
          "receiptNumber": "string",
          "receiptType": "string",
          "refundFor": "string",
          "source": "string",
          "storeId": "string",
          "surcharge": 1,
          "tip": 1,
          "totalDiscount": 1,
          "totalDiscounts": [
            {
              "id": "string",
              "moneyAmount": 1,
              "name": "Ava Chen",
              "percentage": 1,
              "type": "string"
            }
          ],
          "totalMoney": 1,
          "totalTax": 1,
          "totalTaxes": [
            {
              "id": "string",
              "moneyAmount": 1,
              "name": "Ava Chen",
              "rate": 1,
              "type": "string"
            }
          ],
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `receipts` | array<object> |  |
| `receipts[].cancelledAt` | date | The time when this receipt was cancelled |
| `receipts[].createdAt` | date | The autogenerated date and time when the receipt was created in Loyverse. |
| `receipts[].customerId` | string | The customer id associated with the receipt |
| `receipts[].diningOption` | string | The dining option selected for the receipt |
| `receipts[].employeeId` | string | The employee id associated with the receipt |
| `receipts[].lineItems` | array<object> | The line items included in the receipt |
| `receipts[].lineItems[].cost` | number | The cost of the single item at the moment of transaction |
| `receipts[].lineItems[].costTotal` | number | The total cost for this line item at the moment of transaction |
| `receipts[].lineItems[].grossTotalMoney` | number | The total money amount for this line item including modifiers. It doesn't include discounts and taxes which type is ADDED. |
| `receipts[].lineItems[].id` | string | The unique id that identifies this line item in the receipt |
| `receipts[].lineItems[].itemId` | string | The item id for this line item |
| `receipts[].lineItems[].itemName` | string | The item name |
| `receipts[].lineItems[].lineDiscounts` | array<object> | The list of discounts applied to the line item |
| `receipts[].lineItems[].lineDiscounts[].id` | string | The discount id |
| `receipts[].lineItems[].lineDiscounts[].moneyAmount` | number | The money amount of this discount for the line item. The value is always positive. |
| `receipts[].lineItems[].lineDiscounts[].name` | string | The discount name |
| `receipts[].lineItems[].lineDiscounts[].percentage` | number | The percentage of the discount. For example value 10.55 corresponds to a percentage of 10.55%. The value is not set for amount based discounts. |
| `receipts[].lineItems[].lineDiscounts[].type` | string | The discount type |
| `receipts[].lineItems[].lineModifiers` | array<object> | The list of modifiers applied to the line item |
| `receipts[].lineItems[].lineModifiers[].id` | string | The modifier id |
| `receipts[].lineItems[].lineModifiers[].modifierOptionId` | string | The modifier option id applied to the line item |
| `receipts[].lineItems[].lineModifiers[].moneyAmount` | number | The total money amount of the modifier applied to the line item. It is equal to the price of the modifier option multiplied by the line item's quantity |
| `receipts[].lineItems[].lineModifiers[].name` | string | The modifier name |
| `receipts[].lineItems[].lineModifiers[].option` | string | The name of the modifier option applied to the line item |
| `receipts[].lineItems[].lineModifiers[].price` | number | The base price of a single modifier option |
| `receipts[].lineItems[].lineNote` | string | The line item note |
| `receipts[].lineItems[].lineTaxes` | array<object> | The list of taxes applied to the line item |
| `receipts[].lineItems[].lineTaxes[].id` | string | The tax id |
| `receipts[].lineItems[].lineTaxes[].moneyAmount` | number | The money amount of this tax for the line item |
| `receipts[].lineItems[].lineTaxes[].name` | string | The tax name |
| `receipts[].lineItems[].lineTaxes[].rate` | number | The rate of the tax. For example, a value of "5.255" corresponds to a percentage of 5.255% |
| `receipts[].lineItems[].lineTaxes[].type` | string |  |
| `receipts[].lineItems[].price` | number | The price of the one item. It includes taxes which type is INCLUDED. It doesn't include modifiers, discounts and taxes which type is ADDED. |
| `receipts[].lineItems[].quantity` | number | The number of items that were purchased (or refunded in case of refund) |
| `receipts[].lineItems[].sku` | string | The variant sku |
| `receipts[].lineItems[].totalDiscount` | number | The total discount amount applied to the line item. The value is always positive. |
| `receipts[].lineItems[].totalMoney` | number | The total money amount for this line item after applying discounts and all taxes for this line item |
| `receipts[].lineItems[].variantId` | string | The variant id for this line item |
| `receipts[].lineItems[].variantName` | string | The variant name (for example XL / Red) |
| `receipts[].note` | string | The receipt's note |
| `receipts[].order` | string | The order name or number associated with this receipt |
| `receipts[].payments` | array<object> | The list of receipt payments |
| `receipts[].payments[].moneyAmount` | number | The total money amount of this payment (including tips and surcharge) |
| `receipts[].payments[].name` | string | The name of the payment type |
| `receipts[].payments[].paidAt` | date | The time when this payment was created |
| `receipts[].payments[].paymentDetails` | object | The payment details for integrated payment types |
| `receipts[].payments[].paymentDetails.authorizationCode` | string | The authorization code associated with the transaction |
| `receipts[].payments[].paymentDetails.cardCompany` | string | The credit card company (if available) |
| `receipts[].payments[].paymentDetails.cardNumber` | string | The masked credit card number |
| `receipts[].payments[].paymentDetails.entryMethod` | string | The entry method of the credit card on the terminal (if available) |
| `receipts[].payments[].paymentDetails.referenceId` | string | An id attached to the transaction by the gateway |
| `receipts[].payments[].paymentTypeId` | string |  |
| `receipts[].payments[].type` | string |  |
| `receipts[].pointsBalance` | number | The customer's points balance after transaction |
| `receipts[].pointsDeducted` | number | The total amount of points deducted from customer's points balance (in case of refund). The value is always positive. |
| `receipts[].pointsEarned` | number | The total amount of points added to customer's points balance |
| `receipts[].posDeviceId` | string | The POS id where the receipt was paid |
| `receipts[].receiptDate` | date | By default, it matches the created_at value. You can set receipt_date to the value that is equal to the date and time in the past when the receipt was created in another system. |
| `receipts[].receiptNumber` | string | The internal identifier for the receipt. It is unique. |
| `receipts[].receiptType` | string | The type of the receipt |
| `receipts[].refundFor` | string | The number of a different sales receipt that is associated with this refund. (Only for refund receipts) |
| `receipts[].source` | string | The name of the the source this receipt comes from. By default it is the name of the application that created the receipt. For receipts created from Loyverse mobile point of sale application the value is "point of sale". |
| `receipts[].storeId` | string | The store id where the receipt was paid |
| `receipts[].surcharge` | number | The total surcharge money amount for the receipt |
| `receipts[].tip` | number | The total tip money amount for the receipt |
| `receipts[].totalDiscount` | number | The total amount of all discounts applied in the receipt (including discount by points). The value is always positive. |
| `receipts[].totalDiscounts` | array<object> | The list of discounts and it's amounts applied to the receipt. |
| `receipts[].totalDiscounts[].id` | string | The discount id |
| `receipts[].totalDiscounts[].moneyAmount` | number | The total money amount of this discount for the receipt. The value is always positive. |
| `receipts[].totalDiscounts[].name` | string | The discount name |
| `receipts[].totalDiscounts[].percentage` | number | The percentage of the discount. For example value 10.55 corresponds to a percentage of 10.55%. The value is not set for amount based discounts. |
| `receipts[].totalDiscounts[].type` | string | The type of the applied discount |
| `receipts[].totalMoney` | number | The total money amount paid by customer (or returned to customer in case of refund). The value includes discounts, taxes, surcharges and tips. The money amount format depends on country of account registration  (for example for Japan there is no decimals in money amounts) |
| `receipts[].totalTax` | number | The total amount of all taxes (VAT and sales tax) applied in the receipt |
| `receipts[].totalTaxes` | array<object> | An array of tax line objects |
| `receipts[].totalTaxes[].id` | string | The tax id |
| `receipts[].totalTaxes[].moneyAmount` | number | The total tax amount applied for the receipt |
| `receipts[].totalTaxes[].name` | string |  |
| `receipts[].totalTaxes[].rate` | number | The tax rate. For example, a value of 5.255 corresponds to a percentage of 5.255% |
| `receipts[].totalTaxes[].type` | string | The tax type |
| `receipts[].updatedAt` | date | The date and time when the receipt was updated. |

## Native endpoint

Through the native Loyverse API, this operation is `GET /receipts` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-receipts.md) for the provider-specific parameters and requirements.

