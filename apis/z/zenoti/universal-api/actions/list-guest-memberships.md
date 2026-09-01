# Zenoti: List Guest Memberships



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-guest-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-guest-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&guestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "guestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-guest-memberships?${params}`, {
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
| `guestId` | string | yes |  |
| `center` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelFeeAmount": {},
      "cancelFeeNextCollectionDate": {},
      "creditAmount": {
        "other": 1,
        "product": 1,
        "service": 1,
        "total": 1
      },
      "creditBalance": {
        "comments": {},
        "other": 1,
        "product": 1,
        "service": 1,
        "total": 1
      },
      "downgradeOptions": [
        {
          "additionalInfo": {},
          "annualFee": 1,
          "canProrate": true,
          "corpoateAccounts": {},
          "customPaymentMembershipDiscount": 1,
          "description": "string",
          "duration": 1,
          "id": "string",
          "isAnnualFeeEnabled": true,
          "isSetupFeeEnabled": true,
          "isUpgrade": true,
          "name": "Ava Chen",
          "price": 1,
          "setupFee": 1,
          "versionId": "string"
        }
      ],
      "expiryDate": {},
      "freezeFeeAmount": {},
      "freezeFeeNextCollectionDate": {},
      "guestpassBalance": 1,
      "guestpassTotal": 1,
      "guestpassType": "string",
      "hasFilledMembershipForms": true,
      "hasMembershipDigitalForm": true,
      "historicalInvoices": [
        {
          "discount": 1,
          "invoice": {
            "id": "string",
            "itemId": {},
            "no": "string",
            "receiptNo": "string",
            "status": 1
          },
          "paymentType": "string",
          "price": 1,
          "pricePaid": 1,
          "promotion": "string",
          "saleBy": "string",
          "saleDate": "string",
          "taxes": 1
        }
      ],
      "htmlBenefits": {},
      "invoice": {
        "id": "string",
        "itemId": "string",
        "no": "string",
        "receiptNo": "string",
        "status": 1
      },
      "invoiceCenterId": "string",
      "isAddonMember": true,
      "isRefunded": true,
      "memberCode": {},
      "membership": {
        "code": "string",
        "description": {},
        "freezeFeeReasonEnabled": true,
        "id": "string",
        "name": "Ava Chen",
        "type": 1
      },
      "memberSince": "2026-05-07T12:00:00.000Z",
      "nextCollectionAmount": 1,
      "nextCollectionDate": "2026-05-07T12:00:00.000Z",
      "products": [
        {
          "benefitProductId": "string",
          "discount": "string",
          "itemId": "string",
          "itemType": 1,
          "parentCategoryId": "string",
          "productBenefitName": "Ava Chen",
          "productBenefitType": "string",
          "productParentCategoryId": {},
          "productSubCategoryId": {}
        }
      ],
      "recurrenceStatus": 1,
      "recurringDetails": {
        "cancelFeeNextCollectionDate": {},
        "cancellationInitiatedOn": "string",
        "cancelledDate": "string",
        "doNotCollectFrom": {},
        "doNotCollectTill": {},
        "endDateOnUnfreeze": {},
        "freezeFeeNextCollectionDate": {},
        "nextAnnualFeeCollectionDateOnUnfreeze": {},
        "nextCollectionDateOnUnfreeze": {},
        "pausedDate": {},
        "pausedTill": {},
        "suspendedOn": {},
        "terminationDate": "string",
        "updateDateScheduled": {},
        "upgradeDowngradeOn": {}
      },
      "redeemable": {},
      "redemptionSettingDetails": {},
      "restrictCrossCenterRedemption": true,
      "services": [
        {
          "accruedOn": "string",
          "balance": 1,
          "discountDetails": {
            "discountType": 1,
            "offpeakDiscount": 1,
            "peakDiscount": 1,
            "postCreditOffpeakDiscount": 1,
            "postCreditPeakDiscount": 1
          },
          "existsInCurrentCenter": true,
          "expired": 1,
          "expiryDate": {},
          "frequncy": "string",
          "isCategory": true,
          "lastUsageDate": {},
          "price": {},
          "redeemableBalance": 1,
          "refundedCredits": 1,
          "service": {
            "bookWithPartialBalance": 1,
            "canBookService": true,
            "duration": 1,
            "hasSegments": true,
            "id": "string",
            "itemType": {},
            "name": "Ava Chen",
            "saleAsPartOfPackageOrMembershipOnly": true
          },
          "serviceBenefitId": "string",
          "total": 1,
          "transfered": 1,
          "used": 1,
          "userMembershipBenefitPk": 1
        }
      ],
      "status": 1,
      "termsAndConditions": "string",
      "userMembershipId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelFeeAmount` | object |  |
| `cancelFeeNextCollectionDate` | object |  |
| `creditAmount.other` | number |  |
| `creditAmount.product` | number |  |
| `creditAmount.service` | number |  |
| `creditAmount.total` | number |  |
| `creditBalance.comments` | object |  |
| `creditBalance.other` | number |  |
| `creditBalance.product` | number |  |
| `creditBalance.service` | number |  |
| `creditBalance.total` | number |  |
| `downgradeOptions[].additionalInfo` | object |  |
| `downgradeOptions[].annualFee` | number |  |
| `downgradeOptions[].canProrate` | boolean |  |
| `downgradeOptions[].corpoateAccounts` | object |  |
| `downgradeOptions[].customPaymentMembershipDiscount` | number |  |
| `downgradeOptions[].description` | string |  |
| `downgradeOptions[].duration` | number |  |
| `downgradeOptions[].id` | string |  |
| `downgradeOptions[].isAnnualFeeEnabled` | boolean |  |
| `downgradeOptions[].isSetupFeeEnabled` | boolean |  |
| `downgradeOptions[].isUpgrade` | boolean |  |
| `downgradeOptions[].name` | string |  |
| `downgradeOptions[].price` | number |  |
| `downgradeOptions[].setupFee` | number |  |
| `downgradeOptions[].versionId` | string |  |
| `expiryDate` | object |  |
| `freezeFeeAmount` | object |  |
| `freezeFeeNextCollectionDate` | object |  |
| `guestpassBalance` | number |  |
| `guestpassTotal` | number |  |
| `guestpassType` | string |  |
| `hasFilledMembershipForms` | boolean |  |
| `hasMembershipDigitalForm` | boolean |  |
| `historicalInvoices[].discount` | number |  |
| `historicalInvoices[].invoice.id` | string |  |
| `historicalInvoices[].invoice.itemId` | object |  |
| `historicalInvoices[].invoice.no` | string |  |
| `historicalInvoices[].invoice.receiptNo` | string |  |
| `historicalInvoices[].invoice.status` | number |  |
| `historicalInvoices[].paymentType` | string |  |
| `historicalInvoices[].price` | number |  |
| `historicalInvoices[].pricePaid` | number |  |
| `historicalInvoices[].promotion` | string |  |
| `historicalInvoices[].saleBy` | string |  |
| `historicalInvoices[].saleDate` | string |  |
| `historicalInvoices[].taxes` | number |  |
| `htmlBenefits` | object |  |
| `invoice.id` | string |  |
| `invoice.itemId` | string |  |
| `invoice.no` | string |  |
| `invoice.receiptNo` | string |  |
| `invoice.status` | number |  |
| `invoiceCenterId` | string |  |
| `isAddonMember` | boolean |  |
| `isRefunded` | boolean |  |
| `memberCode` | object |  |
| `membership.code` | string |  |
| `membership.description` | object |  |
| `membership.freezeFeeReasonEnabled` | boolean |  |
| `membership.id` | string |  |
| `membership.name` | string |  |
| `membership.type` | number |  |
| `memberSince` | date |  |
| `nextCollectionAmount` | number |  |
| `nextCollectionDate` | date |  |
| `products[].benefitProductId` | string |  |
| `products[].discount` | string |  |
| `products[].itemId` | string |  |
| `products[].itemType` | number |  |
| `products[].parentCategoryId` | string |  |
| `products[].productBenefitName` | string |  |
| `products[].productBenefitType` | string |  |
| `products[].productParentCategoryId` | object |  |
| `products[].productSubCategoryId` | object |  |
| `recurrenceStatus` | number |  |
| `recurringDetails.cancelFeeNextCollectionDate` | object |  |
| `recurringDetails.cancellationInitiatedOn` | string |  |
| `recurringDetails.cancelledDate` | string |  |
| `recurringDetails.doNotCollectFrom` | object |  |
| `recurringDetails.doNotCollectTill` | object |  |
| `recurringDetails.endDateOnUnfreeze` | object |  |
| `recurringDetails.freezeFeeNextCollectionDate` | object |  |
| `recurringDetails.nextAnnualFeeCollectionDateOnUnfreeze` | object |  |
| `recurringDetails.nextCollectionDateOnUnfreeze` | object |  |
| `recurringDetails.pausedDate` | object |  |
| `recurringDetails.pausedTill` | object |  |
| `recurringDetails.suspendedOn` | object |  |
| `recurringDetails.terminationDate` | string |  |
| `recurringDetails.updateDateScheduled` | object |  |
| `recurringDetails.upgradeDowngradeOn` | object |  |
| `redeemable` | object |  |
| `redemptionSettingDetails` | object |  |
| `restrictCrossCenterRedemption` | boolean |  |
| `services[].accruedOn` | string |  |
| `services[].balance` | number |  |
| `services[].discountDetails.discountType` | number |  |
| `services[].discountDetails.offpeakDiscount` | number |  |
| `services[].discountDetails.peakDiscount` | number |  |
| `services[].discountDetails.postCreditOffpeakDiscount` | number |  |
| `services[].discountDetails.postCreditPeakDiscount` | number |  |
| `services[].existsInCurrentCenter` | boolean |  |
| `services[].expired` | number |  |
| `services[].expiryDate` | object |  |
| `services[].frequncy` | string |  |
| `services[].isCategory` | boolean |  |
| `services[].lastUsageDate` | object |  |
| `services[].price` | object |  |
| `services[].redeemableBalance` | number |  |
| `services[].refundedCredits` | number |  |
| `services[].service.bookWithPartialBalance` | number |  |
| `services[].service.canBookService` | boolean |  |
| `services[].service.duration` | number |  |
| `services[].service.hasSegments` | boolean |  |
| `services[].service.id` | string |  |
| `services[].service.itemType` | object |  |
| `services[].service.name` | string |  |
| `services[].service.saleAsPartOfPackageOrMembershipOnly` | boolean |  |
| `services[].serviceBenefitId` | string |  |
| `services[].total` | number |  |
| `services[].transfered` | number |  |
| `services[].used` | number |  |
| `services[].userMembershipBenefitPk` | number |  |
| `status` | number |  |
| `termsAndConditions` | string |  |
| `userMembershipId` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET guests/:guestId/memberships` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-guest-memberships.md) for the provider-specific parameters and requirements.

