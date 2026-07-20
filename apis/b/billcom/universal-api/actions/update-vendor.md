# BILL Payables & Receivables: Update Vendor

Updates a vendor in Bill.com.

```
PUT https://connect.mindcloud.co/v1/universal/billcom/latest/actions/update-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Payables & Receivables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/update-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billcom/latest/actions/update-vendor', {
  method: 'PUT',
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
| `data` | string | no | Example: `{"obj":{"entity":"Vendor","id":"00902EGSBSBVBX2wij9k","name":"MindCloud Test1"}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accNumber": {},
      "accountType": "string",
      "acctBalance": 1,
      "acknowledgedEbillBanner": true,
      "acknowledgedEbillError": true,
      "address1": {},
      "address2": {},
      "address3": {},
      "address4": {},
      "addressCity": {},
      "addressCountry": {},
      "addressState": {},
      "addressZip": {},
      "allowConnectedVendorEditAddress": true,
      "amexMerchantCategory": {},
      "autoPayConflict": true,
      "autoSave": {},
      "autoSaveStatus": {},
      "availCredit": 1,
      "balance": 1,
      "bankCountry": {},
      "billCurrency": "string",
      "billSyncPref": "string",
      "cardFundingPurpose": {},
      "combinePymtUpdateSource": "string",
      "companyName": {},
      "connectionSource": "string",
      "contactFirstName": {},
      "contactLastName": {},
      "createdTime": "string",
      "creationSource": "string",
      "default1099Categories": {},
      "description": {},
      "disableLineItemPredictions": true,
      "eBillEligible": true,
      "eBillEnabledStatus": "string",
      "eBillEnablementFailed": true,
      "eligibleForEbills": true,
      "email": {},
      "enabledCombinePayments": true,
      "enableFundedInvite": true,
      "entity": "string",
      "externalBillPayIn12m": {},
      "fax": {},
      "hasBankAccountAutoPay": true,
      "hasRecurringPayments": true,
      "id": "string",
      "informConnectedVendorAddressSyncModified": true,
      "intlPaymentType": "string",
      "invalidCountryCurrencyAtNewVendorSync": true,
      "isAccountNumberRequired": true,
      "isActive": "string",
      "isAddressValidated": true,
      "isLargeSupplierChild": true,
      "isSyncVendorCountryMapped": true,
      "largeBillerId": "string",
      "lastAcctBalanceUpdate": {},
      "lastBalanceUpdate": {},
      "lastIsLargeSupplierUpdate": {},
      "lastPaymentDate": {},
      "mergedIntoId": "string",
      "name": "Ava Chen",
      "nameOnCheck": "Ava Chen",
      "nameOnCheckRemediation": true,
      "networkStatus": {},
      "numberOfInvitesSent": 1,
      "optedOutOfVCardByOrg": true,
      "orgVCardOptOutCustOther": {},
      "orgVCardOptOutCustReason": {},
      "orgVCardStatus": "string",
      "payBy": "string",
      "payDaysBefore": {},
      "paymentCurrency": {},
      "paymentEmail": {},
      "paymentEmails": {},
      "paymentNetworkId": {},
      "paymentPhone": {},
      "paymentPurpose": {},
      "paymentTermId": "string",
      "paymentusAcctToken": {},
      "paymentusAcctToken2": {},
      "paymentusAcctToken3": {},
      "paymentusMerchantId": {},
      "paymentusPmtType": {},
      "phone": {},
      "preferIVADueDateOverDefaultPT": true,
      "preferSDEOverIVAExtractedLineItems": true,
      "prefPmtMethod": "string",
      "prefRemitEmail": "ava@example.com",
      "processorVCardStatus": {},
      "remitEmail": {},
      "sendInviteForPrivateVendor": true,
      "sendNotifications": true,
      "setupAutoPayPrompt": true,
      "shortName": {},
      "since": {},
      "stpProcessor": "string",
      "taxId": {},
      "taxIdType": {},
      "track1099": true,
      "unmodifiedBillsCount": 1,
      "updatedTime": "string",
      "vcardBillerVendorId": "string",
      "vcardDeclineDate": {},
      "vcardEnrollDate": {},
      "vcardProcessor": "string",
      "vccExistingVendorSegment1": true,
      "vccExistingVendorSegment2": true,
      "vccExistingVendorSegment3": true,
      "vccExistingVendorSegment4": true,
      "vendorBankAccountStatus": 1,
      "vendorVCardRemitEmail": {},
      "vendorVCardStatus": "string",
      "vStatusUpdateSource": {},
      "w9Status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accNumber` | object |  |
| `accountType` | string |  |
| `acctBalance` | number |  |
| `acknowledgedEbillBanner` | boolean |  |
| `acknowledgedEbillError` | boolean |  |
| `address1` | object |  |
| `address2` | object |  |
| `address3` | object |  |
| `address4` | object |  |
| `addressCity` | object |  |
| `addressCountry` | object |  |
| `addressState` | object |  |
| `addressZip` | object |  |
| `allowConnectedVendorEditAddress` | boolean |  |
| `amexMerchantCategory` | object |  |
| `autoPayConflict` | boolean |  |
| `autoSave` | object |  |
| `autoSaveStatus` | object |  |
| `availCredit` | number |  |
| `balance` | number |  |
| `bankCountry` | object |  |
| `billCurrency` | string |  |
| `billSyncPref` | string |  |
| `cardFundingPurpose` | object |  |
| `combinePymtUpdateSource` | string |  |
| `companyName` | object |  |
| `connectionSource` | string |  |
| `contactFirstName` | object |  |
| `contactLastName` | object |  |
| `createdTime` | string |  |
| `creationSource` | string |  |
| `default1099Categories` | object |  |
| `description` | object |  |
| `disableLineItemPredictions` | boolean |  |
| `eBillEligible` | boolean |  |
| `eBillEnabledStatus` | string |  |
| `eBillEnablementFailed` | boolean |  |
| `eligibleForEbills` | boolean |  |
| `email` | object |  |
| `enabledCombinePayments` | boolean |  |
| `enableFundedInvite` | boolean |  |
| `entity` | string |  |
| `externalBillPayIn12m` | object |  |
| `fax` | object |  |
| `hasBankAccountAutoPay` | boolean |  |
| `hasRecurringPayments` | boolean |  |
| `id` | string |  |
| `informConnectedVendorAddressSyncModified` | boolean |  |
| `intlPaymentType` | string |  |
| `invalidCountryCurrencyAtNewVendorSync` | boolean |  |
| `isAccountNumberRequired` | boolean |  |
| `isActive` | string |  |
| `isAddressValidated` | boolean |  |
| `isLargeSupplierChild` | boolean |  |
| `isSyncVendorCountryMapped` | boolean |  |
| `largeBillerId` | string |  |
| `lastAcctBalanceUpdate` | object |  |
| `lastBalanceUpdate` | object |  |
| `lastIsLargeSupplierUpdate` | object |  |
| `lastPaymentDate` | object |  |
| `mergedIntoId` | string |  |
| `name` | string |  |
| `nameOnCheck` | string |  |
| `nameOnCheckRemediation` | boolean |  |
| `networkStatus` | object |  |
| `numberOfInvitesSent` | number |  |
| `optedOutOfVCardByOrg` | boolean |  |
| `orgVCardOptOutCustOther` | object |  |
| `orgVCardOptOutCustReason` | object |  |
| `orgVCardStatus` | string |  |
| `payBy` | string |  |
| `payDaysBefore` | object |  |
| `paymentCurrency` | object |  |
| `paymentEmail` | object |  |
| `paymentEmails` | object |  |
| `paymentNetworkId` | object |  |
| `paymentPhone` | object |  |
| `paymentPurpose` | object |  |
| `paymentTermId` | string |  |
| `paymentusAcctToken` | object |  |
| `paymentusAcctToken2` | object |  |
| `paymentusAcctToken3` | object |  |
| `paymentusMerchantId` | object |  |
| `paymentusPmtType` | object |  |
| `phone` | object |  |
| `preferIVADueDateOverDefaultPT` | boolean |  |
| `preferSDEOverIVAExtractedLineItems` | boolean |  |
| `prefPmtMethod` | string |  |
| `prefRemitEmail` | string |  |
| `processorVCardStatus` | object |  |
| `remitEmail` | object |  |
| `sendInviteForPrivateVendor` | boolean |  |
| `sendNotifications` | boolean |  |
| `setupAutoPayPrompt` | boolean |  |
| `shortName` | object |  |
| `since` | object |  |
| `stpProcessor` | string |  |
| `taxId` | object |  |
| `taxIdType` | object |  |
| `track1099` | boolean |  |
| `unmodifiedBillsCount` | number |  |
| `updatedTime` | string |  |
| `vcardBillerVendorId` | string |  |
| `vcardDeclineDate` | object |  |
| `vcardEnrollDate` | object |  |
| `vcardProcessor` | string |  |
| `vccExistingVendorSegment1` | boolean |  |
| `vccExistingVendorSegment2` | boolean |  |
| `vccExistingVendorSegment3` | boolean |  |
| `vccExistingVendorSegment4` | boolean |  |
| `vendorBankAccountStatus` | number |  |
| `vendorVCardRemitEmail` | object |  |
| `vendorVCardStatus` | string |  |
| `vStatusUpdateSource` | object |  |
| `w9Status` | object |  |

## Native endpoint

Through the native BILL Payables & Receivables API, this operation is `POST Crud/Update/Vendor.json` (base URL `https://api.bill.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vendor.md) for the provider-specific parameters and requirements.

